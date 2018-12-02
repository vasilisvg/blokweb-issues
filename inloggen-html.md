# De HTML van de inlog- en accountformulieren

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

## Headings in een formulier

In een `form` gebruik je geen sections met heading zoals `h2` en `h3`, maar `<fieldset>` met als titel een `<legend>`. Dit geeft je extra mogelijkheden tot visuele form-validatie, en ook dit is weer prettig voor mensen die een screen reader gebruiken.

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
</details>
