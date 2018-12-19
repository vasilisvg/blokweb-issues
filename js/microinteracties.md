# Veelvoorkomende JS issues

Hierbij een paar van de issues die we heel vaak tegenkomen

## Zet je `<script>` onderaan de pagina

Als je je `<script>` in de `<head>` zet dan werkt de `querySelector` niet vanzelf. Zet je script dus helemaal onderaan de pagina, net voordat je de body afsluit.

<details>
  <summary>Een paar voorbeelden</summary>

### Werkt wel
In je HTML
````html
	<button>Klik mij</button>
	…
	<script src="js.js"></script>
</body>
````

In je js
````js
document.querySelector('button');
````

### Werkt niet

In je HTML
````
<head>
	<script src="js.js"></script>
</head>
<body>
	<button>Klik mij</button>
````

In je js
````js
document.querySelector('button');
// De button bestaat nog niet als het script wordt aangeroepen
````
</details>