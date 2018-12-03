# Veelvoorkomende algemene HTML issues

Dit zijn dingen die we vaker tegenkomen. Vaak kleine dingetjes, die er toch toe doen.

## Language attribuut

Elk element kan een `lang` attribuut krijgen. Hierdoor weten zoekmachnies en screen readers in wat voor taal het element is geschreven. Als je het `lang` attribuut op het `<html>` element zet dan geeft dat aan dat het hele document in een bepaalde taal staat. Zorg er voor dat dat klopt!

<details>
  <summary>Zie hier voorbeelden</summary>

### Goed

````html
<html lang="nl">
<head>
	<title>Allemaal prachtige verhalen</title>
````

### Niet goed
````
<html lang="en">
<head>
	<title>Allemaal prachtige verhalen</title>
````
</details>

## Kapitalen in je HTML

Soms wil je een kopje helemaal in kapitalen zetten. Dit kan je het beste in CSS doen, dan kan je het later eventueel nog aanpassen.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<h2>Alle 99 verhalen</h2>
````

````css 
h2 {
	text-transform: uppercase;
}
````

### Liever niet
````
<h2>ALLE 99 VERHALEN</h2>
````
</details>

## Gebruik echte content

Natuurlijk kopieer je een `article` op de overzichtspagina als die af is. Dan heb je er meteen een heleboel. Tip: pas de content meteen aan. Zet in elke `article` een andere titel, een ander plaatje. Zorg ook voor lastige content. Sommige koppen zijn lang, ander zijn kort.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<article>
	<h2>Moe</h2>
	<img src="moe.png" alt="Prachtig plaatje van iemand die moe is">
</article>
<article>
	<h2>Toch echt wel enigszins aan de ietwat omslachtige kant</h2>
	<img src="moe.png" alt="Mooi, maar nodeloos complex plaatje">
</article>
````

### Nutteloos
````
<article>
	<h2>Moe</h2>
	<img src="moe.png" alt="">
</article>
<article>
	<h2>Moe</h2>
	<img src="moe.png" alt="">
</article>
<article>
	<h2>Moe</h2>
	<img src="moe.png" alt="">
</article>
````
</details>

## Nette code

Zorg er voor dat je code netjes gestructureerd is. Zorg er voor dat de inspringing klopt. Sommige plugins in code editors zijn hier heel slecht in. Het is beter om dit gewoon even met de hand te doen. Dan loop je je code nog eens na. Altijd een goed idee.

<details>
  <summary>Voorbeelden</summary>

### Goed
````html
<article>
	<h2>Moe</h2>
	<img src="moe.png" alt="Prachtig plaatje van iemand die moe is">
	<footer>
		<ul>
			<li><a href="">Copyright</a></li>
			<li><a href="">Contact</a></li>
		</ul>
	</footer>
</article>
````

### Onduidelijk
````
	<article>
<h2>Moe</h2>
<img src="moe.png" alt="Prachtig plaatje van iemand die moe is">
		<footer>
<ul>
			<li>
<a href="">Copyright</a></li>
				<li>
			<a href="">Contact</a></li>
				</ul>
			</footer>
				</article>
````
</details>