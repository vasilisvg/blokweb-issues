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