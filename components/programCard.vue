<template>
    <a :class="['card', status]" :href="programLink" :style="{ '--start': start, '--end': end }">
      <picture class="image">
        <img :src="imgSrc ? `https://fdnd-agency.directus.app/assets/${imgSrc}` : '/path/to/default/image.jpg'" :alt="programName" loading="lazy" />
      </picture>
  
      <article class="content">
        <div class="title-wrapper">
          <h2 :class="{ overflowing: isOverflowing }" ref="text">{{ programName }}</h2>
        </div>
        <div class="time-stamp">
          <span>{{ time }}</span>
        </div>
      </article>
  
      <div class="visit-url"></div>
    </a>
  </template>
  
  <script>
  export default {
    name: 'ProgramCard',
    props: {
      imgSrc: {
        type: String,
        default: ''
      },
      programName: {
        type: String,
        default: 'Unnamed Program'
      },
      time: {
        type: String,
        default: '00:00 - 00:00'
      },
      programLink: {
        type: String,
        default: '/'
      }
    },
    data() {
      return {
        isOverflowing: false,
        status: '',
        currentTime: new Date().getHours() * 100 + new Date().getMinutes()
      };
    },
    computed: {
      start() {
        return parseInt(this.time.split(' - ')[0].replace(':', '')) / 2.001953;
      },
      end() {
        return parseInt(this.time.split(' - ')[1].replace(':', '')) / 2.001953;
      }
    },
    mounted() {
      const [startTime, endTime] = this.time.split(' - ').map((t) => parseInt(t.replace(':', '')));
      if (startTime <= this.currentTime && this.currentTime <= endTime) {
        this.status = 'active';
      }
      this.checkOverflow();
      window.addEventListener('resize', this.checkOverflow);
    },
    beforeDestroy() {
      window.removeEventListener('resize', this.checkOverflow);
    },
    methods: {
      checkOverflow() {
        if (this.$refs.text.scrollWidth > this.$refs.text.clientWidth) {
          this.isOverflowing = true;
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .card {
    display: flex;
    border-radius: 8px;
    background-color: #fff;
    box-shadow: 0 8px 16px rgba(30, 30, 30, 0.08);
    margin-right: 8px;
    position: relative;
  }
  .card.active {
    box-shadow: 0 0 0 2px inset #fe0170;
  }
  .card .content {
    padding: 2rem;
  }
  .overflowing {
    animation: scrolling-left 20s linear infinite;
  }
  @keyframes scrolling-left {
    0% {
      transform: translateX(0%);
    }
    70% {
      transform: translateX(-100%);
    }
    100% {
      transform: translateX(-100%);
    }
  }
  </style>
  