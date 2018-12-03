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