# Veelvoorkomende CSS issues

Hierbij een paar van de issues die we heel vaak tegenkomen

## Waar definiëer je het lettertype?

Maak zo veel mogelijk gebruik van het DRY-principe (Don’t Repeat Yourself). In CSS is dit goed te doen, dankzij de zogenaamde *cascade* en dankzij *overerving*.

<details>
  <summary>Een paar voorbeelden</summary>

### Goed
````css
body {
	font-family: helvetica, arial, sans-serif;
	font-size: 100%;
	color: black;
	background: papayawhip;
}
/* Lettertype-eigenschappen worden overerfd */
p {
	margin: 0 0 1em;
}
/* Beschrijf alleen de uitzonderingen  */
p:first-of-type {
	font-size: 1.414em;
}
````

### Niet goed

````
body {
	background: papayawhip;
}
p {
	font-family: helvetica, arial, sans-serif;
	font-size: 100%;
	color: black;
}
li {
	font-family: helvetica, arial, sans-serif;
	font-size: 100%;
	color: black;
}
/* Dit wordt een lange CSS op deze manier. En stel dat je toch Times New Roman wil gebruiken, dan moet je dat op veel plekken aanpassen … */
````
</details>


## Gebruik geen `px`

We maken gebruik van flexibele units zoals percentages, `em`, `rem`, `vw`, `vh`, `vmin` en `vmax`. Je zou eventueel `px` kunnen gebruiken voor een `border` die écht altijd maar één pixel dik moet zijn, maar verder kan je beter gebruik maken van flexibele units.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````css
button {
	box-shadow: 0 .3em .6em 0 olivedrab;
}
article {
	max-width: 40em;
}
@media (min-width: 40em) {
	…
}
````

### Niet goed
````
button {
	box-shadow: 0 4px 8px 0 olivedrab;
}
article {
	max-width: 640px;
}
@media (min-width: 640px) {
	…
}
````

### Niet goed
````
/* Gebruik overal flexibele units, ook in mediaqueries */
article {
	max-width: 40em;
}
@media (min-width: 640px) {
	…
}
````
</details>

## Gebruik flexbox of CSS Grid voor layout

Flexbox en grid zijn bedacht om alle mogelijke layout mee te kunnen maken. Ze zijn veel krachtiger dan oude de *hacks* die we vroeger moesten gebruiken,  zoals `float` en `display: inline-block`. Gebruik nooit hacks. Gebruik flexbox en grid.

## Flexbox op een <nav>

Let er op dat `flexbox` niet overerft. Flexbox is van invloed op de *directe kinderen*. Dus als je list-items in een `ul` in een `nav` wil laten flexen, dan werkt het niet als je `display:flex` op de `nav` zet.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<nav>
	<ul>
		<li>Item 1</li>
		<li>Item 2</li>
	</ul>
</nav>
````

````css
nav ul {
	display: flex
}
````

### Dit werkt dus niet
````
<nav>
	<ul>
		<li>Item 1</li>
		<li>Item 2</li>
	</ul>
</nav>
````

````
nav {
	display: flex
}
````
</details>