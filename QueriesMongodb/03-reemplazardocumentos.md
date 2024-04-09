
# Reemplazar Documentos

## Sustituir un documento completo 

```m 
db.libros.replaceOne({_id:2},{titulo:'De la tierra a la luna', autor: 'Julio Verne', editorial:'Terra', precio:100})
```

# Borrar Documentos 

_Dos metodos_

1. deleteOne
1. deleteMany

**Eliminar todo el documento con un id = 2**
```m
db.libros.deleteOne({_id:2})
```

**Eliminar todos los documentos donde la cantidad sea mayoor a 150**
```m
db.libros.deleteMany({cantidad:{$gt:150}})
```

# Expresiones Regulares

**Seleccionar todos los documentos que contengan en el titulo una t**
```m
db.libros.find({titulo: /t/})
```

**Seleccionar todos los documentos donde en el titulo se encuentre la palabra JSON**

```m
db.libros.find({titulo:/JSON/})
```