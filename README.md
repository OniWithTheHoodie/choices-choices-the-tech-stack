# ✏️ Beschrijving 

Ik heb eerder gebruikgemaakt van SvelteKit, waarbij ik een site heb gemaakt voor Triple (Mediahuis).
Nu, voor sprint 15, heb ik de gelegenheid gekregen om een nieuw framework te gebruiken en te leren wat de verschillen zijn tussen het gekozen framework en Svelte.
Ik heb gekozen voor Nuxt.js. Ik heb voor Nuxt (Vue) gekozen omdat het veel wordt gebruikt in het bedrijfsleven, goede performance en toegankelijkheid biedt, en omdat het enkele van dezelfde eigenschappen heeft als SvelteKit.


# 💻 Gebruik

Dit is een leer process voor mij zelf om Nuxt.JS te leren en het ontarmen van werken met Nuxt.js zoals componenten, enhanced images. enzovoort aan de hand van de documentatie van Nuxt probeer ik de mogelijkheden te ontdekken en hiermee te experimenteren. Met dit Experiment bouw ik Triple(Mediahuis) site die ik in Sveltekit hebt gemaakt in Nuxt. De Mediahuis site is een webpagina waar je radio zenders kunt beluisteren met o.a Slam FM, Veronica en NPO. Naast het belusiteren van de radio zenders heb je online gids. Je kunt hierin alle programma's vinden die gedraait worden door de radio zenders. dan zie je de tijden en welke DJ er dan op dat moment draait en een media player die de radio zender afspeelt.

### User story
* Als gebruiker wil ik kunnen zien wanneer alle radioshows worden uitgezonden en welke dj er draait.
* Door op de dagen te klikken, kun je het overzicht ophalen van de radioshows die op die dag worden uitgezonden.
* De radio kunnen afspelen met de mediaplayer.
* Kunnen filteren met aangemaakte knoppen, gebaseerd op - of + uren.

![foto media huis](<Schermafbeelding 2024-10-20 215906.png>)

## 🔎 Kenmerken

### Ontwerp
Het ontwerp dat we van Triple hebben gekregen voor de desktopweergave bevat een header met het logo van Veronica. Dit is in een horizontale lijn geplaatst, zodat er meer radiostations tegelijk kunnen worden bekeken. De mediaplayer wordt groot weergegeven, met informatie over welke dj er draait en de aankomende liedjes. Ook is er een footer aanwezig.
Voor mobiel wordt het een één-kolomslayout voor de gids. De mediaplayer wordt kleiner weergegeven, en de footer verdwijnt en wordt vervangen door een mobiel menu.

### Features

#### Responsive page
Door middel van media queries is de pagina responsive en te gebruiken op elk schermformaat!

#### Image optimalisatie (layout shifting)
De afbeeldingen hebben een standaard breedte en hoogte om layoutverschuiving te voorkomen.

### Technieken
- HTML
@@ -58,16 +59,16 @@ De images hebben een standaard width en height, zodat dit layout shifting voorko

## 🔧 Installatie
<!-- Bij Instalatie staat hoe een andere developer aan jouw repo kan werken -->

Clone deze repository.
Open de repository met een code-editor naar keuze.
Open de terminal in de code-editor.
Typ npx nuxi@latest init in de terminal om alle benodigdheden voor het project te installeren.
De terminal zal na de installatie vragen of je wilt dat er een git-repo voor jou wordt ingericht. Zeg nee, omdat deze repository is gecloned. Als je ja zegt, krijg je een conflict bij het pushen omdat de instellingen worden aangepast, omdat Nuxt/Terminal het voor jou inricht. Zeg dus alleen ja als je een eigen aparte repository maakt vanuit deze repo.
Verander het pad van het project naar cd nuxt-app om het te kunnen openen.
Om het project te openen, typ je in de terminal: npm run dev of npm run dev -- -o om de server op te starten.
Gebruik de link <a href="http://localhost:3000/">localhost</a> om het project lokaal te bekijken.
Mocht je het project online bekijken, dan kan dat via <a href="https://choices-choices-the-tech-stack-lovat.vercel.app/" alt="link naar de website">deze link</a>.
## 👨‍💻 Bronnen
- <a href="https://nuxt.com/docs/getting-started/introduction">Nuxt js documentatie</a>