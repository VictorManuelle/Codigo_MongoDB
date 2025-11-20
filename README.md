# Codigo_MongoDB
Codigo trabajado dentro de MongoDB
# Archivos usados:
MongoDB 8.2.1
Datos publicos de entidad de gas
https://www.datos.gov.co/resource/ek3f-5wn4.csv

# En MongoDb se debe crear la conexión de nuestros datos

En mi caso la llame Gas_natural, despues creamos la base de datos en create database que le di el nombre de Gas y en collection name le coloque el nombre de contratos.
Despues de eso dentro de contratos le damos a import data y colocamos los datos que encontramos en archivos usados de los datos publicos de entidad de gas, que es un archivo (csv). 

# Documentación del diseño de la base de datos
campos principales:

_id: Identificador unico.
ano: Año vigente de la tarifa.
mes: Mes que aplica la tarifa.
empresa: Nombre de la empresa que presta el servicio.
municipios: Lista de municipio donde la empresa presta el servicio.
nit: Identificador unico de la empresa ante la Dian.
id_empresa: Codigo que el sistema le asigna a la empresa.
id_mercado: Codigo que identifica la zona o mercado donde opera.
estrato: Estrato socioeconomico al que se le aplica la tarifa (1-6).
conexion: Costo para instalar el servicio por primera vez.
reinstalacion: Costo para reinstalar el servicio despues de una suspención.
reconexion: Costo por reconexión despues de suspencion temporal
cargo_fijo: Cuota mensual fija.
rango_0: Tarifa para los primeros 20m cubicos mensuales
rango_21: Tarifa para consumos superiores a 20m cubicos mensuales

# Dentro de cada codigo se encuentra la explicación



