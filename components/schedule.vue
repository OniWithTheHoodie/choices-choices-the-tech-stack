<template>
    <div class="schedule">
      <template v-if="Object.keys(groupedShows).length > 0">
        <div v-for="(stationShows, stationName) in groupedShows" :key="stationName" class="schedule__radio-station-row">
          <div class="schedule__station-shows">
            <ProgramCard
              v-for="(show, i) in stationShows"
              :key="show.id"
              :programName="show.mh_shows_id?.show?.name || 'Onbekende programma'"
              :time="getShowTime(show)"
              :imgSrc="getImageSource(show)"
              :programLink="`/shows/${show.id}`"
              :i="i"
            />
          </div>
        </div>
      </template>
      <p v-else>Er zijn geen programma's</p>
    </div>
  </template>
  
  <script>
  import ProgramCard from './programCard.vue';
  
  export default {
    name: 'Schedule',
    props: {
      data: {
        type: Object,
        required: true
      }
    },
    components: {
      ProgramCard
    },
    computed: {
      groupedShows() {
        return this.groupByRadioStation(this.data?.data?.[0]?.shows || []);
      }
    },
    methods: {
      getImageSource(show) {
        const programShow = show.mh_shows_id?.show;
        const firstUser = programShow?.users?.[0]?.mh_users_id?.cover;
        const thumbnail = programShow?.thumbnail?.id;
        return firstUser ? `/${firstUser}` : thumbnail ? `/${thumbnail}` : '';
      },
      getShowTime(show) {
        const showId = show.mh_shows_id;
        const from = showId?.from ? showId.from : '00:00';
        const until = showId?.until ? showId.until : '00:00';
        return `${from.slice(0, 5)} - ${until.slice(0, 5)}`;
      },
      groupByRadioStation(shows) {
        const radioStation = {};
        shows.forEach((show) => {
          const programShow = show.mh_shows_id?.show;
          const stationName = programShow?.radiostation?.name || 'Unknown Station';
          if (!radioStation[stationName]) radioStation[stationName] = [];
          radioStation[stationName].push(show);
        });
  
        Object.keys(radioStation).forEach((stationName) => {
          radioStation[stationName].sort((a, b) => {
            const fromA = a.mh_shows_id?.from || '00:00';
            const fromB = b.mh_shows_id?.from || '00:00';
            return fromA.localeCompare(fromB);
          });
        });
  
        return radioStation;
      }
    }
  };
  </script>
  
  <style scoped>
  .schedule {
    display: grid;
    grid-gap: 1em;
    overflow: scroll;
    padding: 2rem;
  }
  .schedule__station-shows {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  }
  </style>
  