# Busquedas condicionales

# Operadores de Comparación 
   | Operador | Descripción | 
   | -- | -- |
   | $eq | igual |
   | $gt | Mayor que |
   | $gte | Mayor o Igual |
   | $in | Buscar un elemento en un array |
   | $lt | Menor que |
   | $lte | Menor o Igual |
   | $ne | Todos los elementos que no sean iguales |
   | $nin | Ninguno de los valores del arreglo |

## Busquedas

_Selecciona todos los documentos de una coleccion_
```m
db.libros.find()
db.libros.find({})
```

_Seleccionar todos los documentos de la coleccion libros donde la editorial sea Biblio_


```m
db.libros.find({editorial:'Biblio'})
```

_Seleccionar todos los documentos de la coleccion libros donde el precio sea igual a 25_

``` m
 db.libros.find({precio:25})
```

## Busquedas con operadores logicos

**Sintaxis**
```
{<columna>:{<operador>:<valor>}, ...}
```

_Seleccionar todos aquellos documentos de la coleccion libros donde el precio sea mayor a 25_

```m
db.libros.find({precio:{$gt:25}})
```