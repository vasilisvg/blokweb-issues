# De HTML van de inlog- en accountformulieren

Deze issues zien we vaak. Wellicht heb jij ze ook?

## Labels zitten niet gekoppeld aan inputs

### Wrong
````
<label>naam</label>
<input id="naam">
````

### Goed
````css
<label>
  Naam
  <input>
</label>
````

### Ook goed
````css
<label for="naam">naam</label>
<input id="naam">
````
