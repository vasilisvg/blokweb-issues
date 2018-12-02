# De HTML van de inlog- en accountformulieren

Deze issues zien we vaak. Wellicht heb jij ze ook?

## Labels zitten niet gekoppeld aan inputs

Labels moet je koppelen aan inputs. Je krijgt dan helemaal gratis allemaal lagen van UX er bij. En bovendien kunnen mensen met een screenreader je form nu ook invullen!

<details>
  <summary>Zie wat voorbeelden</summary>

### Niet goed
````
<label>naam</label>
<input id="naam">
````

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
</details>
