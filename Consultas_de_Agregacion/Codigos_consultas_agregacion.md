# Nuestros datos vienen de este documento que lo conectamos a MongoDB
https://www.datos.gov.co/resource/ek3f-5wn4.csv

# MongoDb trabaja con lenguaje javascript

# Esto lo trabajaremos desde la parte de Aggregation en MongoDB
```javascript

//Los Stage los creamos en Add stage

# Stage 1 $group

{
  "_id": null, //Agrupar todos los documentos
  "total_contratos": { "$sum": 1 },//Conteo total
  "suma_total_cargo_fijo": { "$sum": "$cargo_fijo" },
   "promedio_cargo_fijo": { "$avg": "$cargo_fijo" },
    "max_cargo_fijo": { "$max": "$cargo_fijo" },
  "min_cargo_fijo": { "$min": "$cargo_fijo" }
}

# Stage 2 $project

{
  "_id": 0,// Esto es para excluir el campo _id
  "total_contratos": 1,
  "suma_total_cargo_fijo": { "$round": ["$suma_total_cargo_fijo", 2] },
   "promedio_cargo_fijo": { "$round": ["$promedio_cargo_fijo", 2] },
   "rango_cargo_fijo": {
    "maximo": "$max_cargo_fijo",
    "minimo": "$min_cargo_fijo",
    "diferencia": { "$subtract": ["$max_cargo_fijo", "$min_cargo_fijo"] }
  }
}

/*Con estos datos vemos una base grande de contratos que en mi caso serían 1000 contratos.
 Se puede ver unos ingresos estables de aproximadamente $2.6 millones mensuales. Lo malo que puedo ver
 es la diferencia que hay entre el máximo y mínimo ya que los de máximo es $8264 y el mínimo es de 0 
 lo que nos puede indicar que hay errores o que algunas personas no se les cobre y esto genera 
 que los usuarios paguen unos precios muy diferentes.*/



