# Nuestros datos vienen de este documento que lo conectamos a MongoDB
https://www.datos.gov.co/resource/ek3f-5wn4.csv

# MongoDb trabaja con lenguaje javascript
``` javascript

# Codigo de Inserción

//Este codigo lo digitamos desde MongoDB shell

db.contratos.insertOne({
  "id_contrato": "TEST-01",//Aqui en id_contrato para esta prueba elegi el nombre de TEST-01
  "empresa": "EMPRESA DE PRUEBA Unad S.A.", 
  "estrato": 2,
  "cargo_fijo": 3500,
  "departamento": "BOGOTA",
  "año": 2024,
  "fecha_insercion": new Date()// Aqui nos colocara la fecha actual en el que creamos este documento
})

//Con este codigo lo que hacemos es crear un nuevo documento en nuestra base de datos

# Codigo de Seleccion
//Este codigo lo podemos digitar desde Documents en la parte de Type a Query
{"id_contrato": "TEST-01"}

//Este nos sirve para seleccionar un tipo de dato en especifico y para ver si se guardo correctamente

# Codigo Actualización
//Este codigo lo digitamos desde MongoDB shell
db.contratos.updateOne(
  { "id_contrato": "TEST-01" },
  { 
    $set: { 
      "cargo_fijo": 4000,
      "fecha_actualizacion": new Date()
    } 
  }
)

# Codigo Eliminación
//Este codigo lo digitamos desde MongoDB shell

db.contratos.deleteOne({ "id_contrato": "TEST-01" })

//Con este codigo se puede observar que borramos nuestro documento TEST-01
