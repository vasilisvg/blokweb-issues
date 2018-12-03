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
````html
<img src="naam-van-plaatje-ghjhjlfhulisdfl-1234.png">
<!-- Nu wordt de src voorgelezen. Probeer maar. -->
````