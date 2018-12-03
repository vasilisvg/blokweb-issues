# Overzichtspagina

Deze issues zien we vaak. Wellicht heb jij die ook, of diegene die je feedback gaat geven.

## Een zoekveld staat in een formulier

We zien wel eens een los zoekveld in de code staan. Of in een `div` of een `section`. Zoekvelden horen in een `form` te staan, anders werken ze niet.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<form action="zoekresultaten.html">
	<label>Zoeken
		<input type="search">
	</label>
	<button>Zoek!</button>
</form>
````

### Niet goed
````
<section>
	<input type="text" placeholder="Zoeken..">
</section>
````
</details>

## Een `img` moet een `alt` attribuut hebben

Er je geen alt-attribuut in een `img` zet dan is dat onhandig voor mensen die om wat voor reden dan ook geen plaatjes kunnen zien. Dat zijn bijvoorbeeld mensen die in de trein langs Abcoude rijden, maar natuurlijk ook blinde mensen. In deze situaties krijg je de inhoud van het alt-attribuut te zien/horen. Zorg er dus voor dat dit een echte omschrijving van het plaatje is. 

Als er geen alt-attribuut in staat dan wordt de `src` van het plaatje voorgelezen/getoond. Dat wil je niemand aandoen.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<img src="naam-van-plaatje-ghjhjlfhulisdfl-1234.png" alt="Foto van een slapende kat">
````

### Soms goed
````html
<img src="naam-van-plaatje-ghjhjlfhulisdfl-1234.png" alt="">
<!-- Als een alt leeg is wordt het plaatje genegeerd door screen readers -->
````

### Niet goed
````
<img src="naam-van-plaatje-ghjhjlfhulisdfl-1234.png">
<!-- Nu wordt de src voorgelezen. Probeer maar. -->
````
</details>

## Een heading van een section staat er in, niet er boven

Soms zie ik een heading van een section net vóór de section staan. De heading hoort er in te staan.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<section>
	<h2>De nieuwste verhalen</h2>
	…
</section>
````

### Dus niet
````
<h2>De nieuwste verhalen</h2>
<section>
	…
</section>
````
</details>

## Er mag maar één `h1` op een pagina staan

Over het algemeen is de `h1` de titel van de pagina. Dus op de overzichtspagina zou dat iets kunnen zijn als `<h1>Allemaal hele mooie dezelfde maar toch andere verhalen</h1>`. 

## Elke section heeft een heading

Een section is een thematische groepering van dingen. Zo'n groepering heeft altijd een titel. Bijvoorbeeld *Meest gelezen verhalen*, of *Resultaten van filteren en sorteren*. Soms komt het voor dat je zo'n titel eigenlijk niet visueel nodig hebt. Zet hem in dat geval toch in de HTML, maar verberg hem met CSS.

Dit geldt ook voor een article. Die moet ook altijd een heading.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<section>
	<h2>De nieuwste verhalen</h2>
	<article>
		<h3>Moe</h3>
		…
	</article>
	<article>
		<h3>Wakker</h3>
		…
	</article>
</section>
````

### Niet goed
````
<section>
	<article>
		<h2>Moe</h2>
		…
	</article>
	<article>
		<h2>Wakker</h2>
		…
	</article>
</section>
````
</details>

## Zet metadata in een footer

Ja, elke article kan een `<footer>` hebben. Een footer hoeft niet alleen onderaan een pagina te staan: in een footer zet je metadata. Als de footer in een article staat, dan is het metadata over dat article, zoals bijvoorbeeld *auteur, en datum*.


<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<article>
	<h3>Moe</h3>
	<footer>
		<ul>
			<li>Geestig</li>
			<li>13 zinnen</li>
			<li>12.08/2016</li>
		</ul>
	</footer>
</article>
<!-- Hier is het duidelijk dat dit geen content is, maar metadata -->
````

### Niet goed
````
<article>
	<h3>Moe</h3>
	<ul>
		<li>Geestig</li>
		<li>13 zinnen</li>
		<li>12.08/2016</li>
	</ul>
</article>
<!-- Hier is het onduidelijk: is dit content, of metadata? -->
````
</details>
