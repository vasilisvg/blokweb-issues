# De HTML van de formulieren

Met formulieren kan je data uitwisselen tussen de gebruiker en de server. Zonder formulieren kan je niet shoppen, is er geen Moodle, en bestond er geen Github.

Deze issues zien we vaak. Wellicht heb jij ze ook?

## Labels zitten niet gekoppeld aan inputs

Labels moet je koppelen aan inputs. Je krijgt dan helemaal gratis allemaal lagen van UX er bij. En bovendien kunnen mensen met een screenreader je form nu ook invullen!

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<label>
  Naam
  <input>
</label>
````

### Ook goed
````html
<label for="naam">naam</label>
<input id="naam">
````

### Niet goed
````
<label>naam</label>
<input id="naam">
````
</details>

## Hoe doe je headings in een formulier

In een `form` gebruik je *nooit* `<section>` met headings zoals `h2` en `h3`, maar `<fieldset>` met als titel een `<legend>`. Dit geeft je extra mogelijkheden tot visuele form-validatie, en ook dit is weer prettig voor mensen die een screen reader gebruiken.

*Overigens kan je fieldsets ook prima nesten. Een fieldset in een fieldset kan dus, mocht je het nodig hebben.*

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<form>
  <fieldset>
    <legend>Inloggen</legend>
    <label>Naam<input></label>
    <label>Email<input type="email"></label>
  </fieldset>
  <button>Verstuur</button>
</form>
````

### Niet goed
````
<form>
  <h2>Inloggen</h2>
  <label>Naam<input></label>
  <label>Email<input type="email"></label>
  <button>Verstuur</button>
</form>
````
### Ook niet goed
````
<form>
  <section>
    <h2>Inloggen</h2>
    <label>Naam<input></label>
    <label>Email<input type="email"></label>
    <button>Verstuur</button>
  <section>
</form>
````
</details>

## Een fieldset staat in een formulier, niet andersom

Soms zien we een `fieldset` die om een `form` heen staat. Een `fieldset` is een sectie van een `form`, en dus moeten die er in staan.

<details>
  <summary>Zie wat voorbeelden</summary>

### Goed
````html
<form action="/action_page.php">
  <fieldset>
    <legend>Formulier</legend>
    <label>Login naam:<input type="text"></label>
    <label>Paswoord:<input type="password"></label>
    <input type="submit" value="Submit">
  </fieldset>
</form>
````

### Niet goed
````
<fieldset>
  <legend>Formulier</legend>
  <form action="/action_page.php">
    <label>Login naam:<input type="text"></label>
    <label>Paswoord:<input type="password"></label>
    <input type="submit" value="Submit">
  </form>
</fieldset>
````
</details>
