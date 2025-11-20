# Nuestros datos vienen de este documento que lo conectamos a MongoDB
https://www.datos.gov.co/resource/ek3f-5wn4.csv

# MongoDb trabaja con lenguaje javascript
```javascript

# $eq - Igual a
//Este codigo lo podemos digitar desde Documents en la parte de Type a Query

{ "estrato": { "$eq": 1 } }

//nos mostrara los estratos igual a 1

# $gt - Mayor que
//Este codigo lo podemos digitar desde Documents en la parte de Type a Query

{ "cargo_fijo": { "$gt": 2000 } }

//Nos mostrara el cargo fijo mayor que 2000

# $lt - Menor que  
//Este codigo lo podemos digitar desde Documents en la parte de Type a Query

{ "cargo_fijo": { "$lt": 3000 } }

//Nos mostrara cargo fijo menor que 3000

# $exists – Verifica si el campo existe
//Este codigo lo podemos digitar desde Documents en la parte de Type a Query

{ "conexion": { "$exists": true } }

//Sirve para verificar que todos los registros tengan costo de conexion 


