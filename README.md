> _Fork_ deze leertaak en ga aan de slag. 
Onderstaande outline ga je gedurende deze taak in jouw eigen GitHub omgeving uitwerken. 
De instructie vind je in: [docs/INSTRUCTIONS.md](https://github.com/fdnd-task/choices-choices-the-tech-stack/blob/main/docs/INSTRUCTIONS.md)

# Nuxt.js(VUE)

## Inhoudsopgave
  * [✏️ Beschrijving](##beschrijving)
  * [💻 Gebruik](##gebruik)
  * [🔎 Kenmerken](##kenmerken)
  * [🔧 Installatie](##installatie)
  * [📊 Projectboard] (##projectboard)
  * [👨‍💻 Bronnen](##bronnen)

# ✏️ Beschrijving 

Ik heb voorheen kennis gemaakt met het sveltekit waarbij ik de site heb gemaakt voor Triple(Mediahuis).
Nu voor sprint 15 heb ik de gelegeheid gekregen om een nieuwe framework te gebruiken en te leren wat de verschillen zijn tussen de gekozen framework en svelte.
Ik heb gekozen voor Nuxt.js. Ik heb voor Nuxt(Vue) gekozen omdat het veel wordt gebruikt in het bedrijfs leven, performance, toegangkelijkheid en ook omdat het paar van de zelfde eigenschappen heeft als Sveltekit. 


# 💻 Gebruik

Dit is een leer process voor mij zelf om Nuxt.JS te leren en het ontarmen van werken met Nuxt.js zoals componenten, enhanced images. enzovoort aan de hand van de documentatie van Nuxt probeer ik de mogelijkheden te ontdekken en hiermee te experimenteren. Met dit Experiment bouw ik Triple(Mediahuis) site die ik in Sveltekit hebt gemaakt in Nuxt. De Mediahuis site is een webpagina waar je radio zenders kunt beluisteren met o.a Slam FM, Veronica en NPO. Naast het belusiteren van de radio zenders heb je online gids. Je kunt hierin alle programma's vinden die gedraait worden door de radio zenders. dan zie je de tijden en welke DJ er dan op dat moment draait en een media player die de radio zender afspeelt.

### User story
* Als gebruiker wil ik kunnen zien wanneer alle radioshows spelen en welke dj er draait.
* Door op de dagen te klikken kun je het overzicht van de radioshows die op die dag spelen ophalen.
* Radio afkunnen spelenn met de mediaplayer
* kunnen filteren met aangemaakte buttons gebaseerd op - of + uren.

![foto media huis](<Schermafbeelding 2024-10-20 215906.png>)

## 🔎 Kenmerken

### Ontwerp
Het ontwerp van Triple gekregen voor desktop view bevat een header met de logo van Veronica, is in een horizontale lijn gezet zodat er meer radiostations in een keer te bekijken zijn, media player wordt in het groot weergeven, welke dj er draait, opkommende liedjes en de footer.
Voor mobiel zal dat een one column layout zijn voor de gids, media player wordt in het klein weergeven en de footer verdwijnt en wordt een mobiele menu. 

### Features

#### Responsive page
Doormiddel van media queries is de pagina responsive en te gebruiken op elk scherm formaat!

#### Image optimalisatie (layout shifting)
De images hebben een standaard width en height, zodat dit layout shifting voorkomt.

### Technieken
- HTML
- CSS
- JS
- Nuxt.js(Vue)

### Tools
- Visual studio code (code editor)
- Vercel (hosting)
- Figma (Design tool)

## 🔧 Installatie
<!-- Bij Instalatie staat hoe een andere developer aan jouw repo kan werken -->
1. Clone deze repository
2. Open de repository met een code editor naar keuze
3. Open het terminal in de code editor
4. Typ **npx nuxi@latest init** in om alle benodigdheden voor het project te installeren in de terminal
5. Zal de terminal na de installatie vragen of je wilt dat er git repo voor jou wordt ingericht. Zeg nee omdat deze repository is gecloned, als je ja zegt krijg je een conflict bij het pushen omdat de instellingen worden aangepast omdat Nuxt/Terminal het voor jou inricht. Dus alleen ja zeggen als je eigen aparte repository maakt vanuit deze repo.
6. verander het pad van het project naar `cd nuxt-app` om het te kunnen opennen
7. Om het project te kunnen openen type je in de terminal: `npm run dev` of `npm run dev -- -o` om de server op te starten
8. Gebruik de link <a href="http://localhost:3000/">localhost</a> om het project lokaal te bekijken
9. Mocht je het project online bekijken dan kan dat via <a href="https://choices-choices-the-tech-stack-lovat.vercel.app/" alt="link naar de website">deze link</a>

## 👨‍💻 Bronnen
- <a href="https://nuxt.com/docs/getting-started/introduction">Nuxt js documentatie</a>

- <a href="https://image.nuxt.com/get-started/installation">Nuxt enhanced images</a>

- <a href="https://nuxt.com/docs/getting-started/data-fetching">Nuxt fetching data</a>
