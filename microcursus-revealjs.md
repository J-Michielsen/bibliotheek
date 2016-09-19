# Micro-cursus reveal.js

Geschreven door Kristof Michiels (versie 0.5, 16.09.2016)

## Wat is reveal.js?

Reveal.js is een krachtig raamwerk dat je toelaat HTML presentaties te maken. Het raamwerk is open source, doet al het zware werk en biedt een uitgebreide set extra's waaronder bvb. aanraakfuncties bij schermen die dat toelaten (Presentations look great on touch devices, like mobile phones and tablets. Simply swipe through your slides.) en tal van geavanceerde slide-overgangen. Jij gaat enkel werken in het HTML-bestand. Indien je een eigen stijl voor je slides wil ontwikkelen, komt er ook CSS aan te pas. Eens je presentatie klaar is kan je ze dan naadloos verwerken in webpagina's en web sites. Er is ook een manier om de presentaties achteraf op te slaan als PDF. 

### Bronnen

- [Website met geïntegreerde demo-presentatie](http://lab.hakim.se/reveal-js/)
- [Bronbestanden en documentatie](https://github.com/hakimel/reveal.js)
- Lynda: [Online Presentations with reveal.js door Ray Villalobos](https://www.lynda.com/CSS-tutorials/Online-Presentations-reveal-js/137904-2.html) 
- [Een oplijsting van voorbeeld-presentaties](https://github.com/hakimel/reveal.js/wiki/Example-Presentations) 


## Snel op weg met Reveal.js

Je download eerst moet je de reveal-bestanden. Het zip-bestand bevat volgende folders: css (styling), js (javascript bestanden), plugin
(bevat componenten die als een reveal.js extensie werden ontwikkeld), lib (alle andere los van reveal ontwikkelde bronnen).

Je maakt een presentatie als html-bestand. In de head sectie dien je te linken naar de algemene stijl en ook naar het thema dat je wenst te gebruiken. Beschikbare thema's zijn o.m.: default, sky, beige, simple, serif, night, moon en solarized. 

``` html
<link rel="stylesheet" href="css/reveal.min.css">
<link rel="stylesheet" href="css/theme/default.css" id="theme">
```

En voor het sluiten van de body tag ga je volgende JavaScript linken:

``` html
<script src="lib/js/head.min.js"></script>
<script src="js/reveal.min.js"></script>
```

Je kan dit bekijken en onderzoeken in de bijgeleverde demopresentatie (demo.html). Deze file onderzoeken en aanpassen is een goede manier om vertrouwd te geraken met dit raamwerk.

Hier vind je voorbeeld hier waarin we drie eenvoudige slides maken met een beperkt aantal HTML-codes. Er zijn drie belangrijke elementen die je gebruikt om de slides voor de presentaties te maken: \<div class="reveal">, \<div class="slides"> en \<section>.

In de <section> tag specificeer je de inhoud van de slides. Standaard beweegt een slide horizontaal. Indien je verticale slides wenst te maken, voeg dan gewoon een nieuwe <section> toe binnen de bestaande. Bvb:

``` html
<div class="reveal">
    <div class="slides">
        <section>Dit is een horizontale slide</section>
        <section>
            <section>En dit is een verticale slide</section>
        </section>
    </div>
</div>
```

In de eerste slide gaan we de intro stoppen... We doen dit met gewone HTML. Een h1-element en een h3 element.

``` html
<section>
  <h1>Mijn presentatie</h1>
  <h3>Hallo dit is een demo over Reveal.js</h3>
</section>
```


Voor de tweede slide werken we met fragmenten. Je doet dit op de volgende manier, met een section (met id="fragments") binnen de eerste section:

``` html
<section>
  <section id="fragments">
    <h2>Ik werk in trapjes</h2>
    <p>Druk op de pijltjes om me langzaam zichtbaar te zien worden!</p>
    <p class="fragment">Ik ben nummer 1</p>
    <p class="fragment">En ik ben nummer 2</p>
    <p class="fragment">Ik ben nummer 3.</p>
  </section>
</section>
```

Enz. Nadat je alle slides hebt gemaakt, dan is de laatste stap de presentatie laten werken door de volgende configuratie toe te voegen aan je html-bestand.

``` html
<script>
  Reveal.initialize({
    controls: true,
    progress: true,
    history: true,
    center: true,
  });
</script>
```

Dit is het enige wat je nodig hebt voor een standaard implementatie. Door goed te kijken naar de voorbeelden, door zelf te experimenteren en de handleiding (zie bronnen) erbij te nemen zal ook jij in staat zijn om fantastische presentaties te maken.
