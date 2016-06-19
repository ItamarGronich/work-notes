# Drupal Notes

## Hooks

* **Update** - updates the given module once when run.
namespace: `function my_module_uopdate_n() {}`


## Use Drupal Services

* **Create a DB query** - `new EntityFieldQuery();` searches the db with assigned properties. query takes certain properties that the query would use to search the DB. To execute the query use `execute()`
``` PHP
$result = $query
  ->entityCondition('condition', 'value')
  ->propertyCondition('condition', value, 'operator')
  ->execute()
```
* **create a wrapper for accessing fields** - `entity_metadata_wrapper($type, $data)` wraps the entity with methods to conveniently get fields from it. also has methods for updating it in the DB.


## Updating a Feature
if you updated a feature you must export it as a feature. using features
drush fu '<feature namespace>'
