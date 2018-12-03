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