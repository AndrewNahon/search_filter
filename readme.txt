A Filtering program using JS and Data Attributes.
1. The catalog of games is stores as an array of objects in the js file. 
2. Each game from the catalog is a list item with an data-id attribute equal to id property on object in catalog.
3. Checkboxes with values for the different types of games systems are used for filtering.
4. On a change event on the checkbox, we first get the value of the box that was clicked. 
5. We then we use filter to get an array of the catalog objects with system equal to that of the checkbox.

  var category = $(this).val();
  var items = catalog.filter(function(item)) {
    return category === item.category
  }

6. Finally we iterate through items, toggling each li with a data-id equal to that of the item.id.

category_items.forEach(function(item) {
  var id = +item.id;
  $games.filter("[data-id=" + id + "]").toggle();
});



