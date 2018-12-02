# De HTML van de inlog- en accountformulieren

Deze issues zien we vaak. Wellicht heb jij ze ook?

## Labels zitten niet gekoppeld aan inputs

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
