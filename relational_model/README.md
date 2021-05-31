

<img src="https://ciudadesabiertas.es/assets/img/cabiertas/logo.svg" alt="LogoCiudadesAbiertas" width="200"/> 

# DESARROLLO API REST DE DATOS REUTILIZABLE. MODELO DE TABLAS: BICICLETA PÚBLICA

&nbsp;

## **ÍNDICE**   
1. [AUTORES](#id1)
2. [LINKS](#id2)
3. [DIAGRAMA CONCEPTUAL](#id3)
4. [TABLAS](#id4)  
    - [BICI_ESTACION](#id5)  
    - [BICI_ANCLAJE](#id6)  
    - [BICI_SENSOR](#id7)  
    - [BICI_OBSERVACION](#id8) 
    - [BICI_BICICLETA](#id9) 
    - [BICI_USUARIO](#id10)  
    - [BICI_TRAYECTO](#id11) 
    - [BICI_PUNTO_PASO](#id12)
5. [TAXONOMÍAS SKOS](#id13)
   - [TIPO-MODELO-BICICLETA](#id14)
   - [TIPO-ESTADO-ANCLAJE](#id15)
   - [TIPO-ESTADO-ESTACION](#id16)
   - [TIPO-ESTADO-BICICLETA](#id17)
   - [TIPO-EQUIPAMIENTO](#id18)




&nbsp;

## AUTORES <a name="id1"></a>
- Edna Ruckhaus
- Francisco Yedro
- Hugo Lafuente Matesanz
- Leticia Rubalcaba
- Oscar Corcho
- Paola Espinoza Arias

&nbsp;

## LINKS <a name="id2"></a>


Este documento contiene la información detallada del modelo de datos asociado al vocabulario de los convenios. A continuación, se detallan los enlaces de interés asociados a este vocabulario:

- *[Documentación](http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica/doc/index-es.html)*
- *[Repositorio](https://github.com/CiudadesAbiertas/vocab-transporte-bicicleta-publica)*
- *[Webinar](https://youtube.com/playlist?list=PLuvmjKgQP8bWHYXc-BvftMLWmPPKQJytu)*
- *[Requisitos](https://github.com/CiudadesAbiertas/vocab-transporte-bicicleta-publica/blob/master/requirements/Requisitos-Bicicleta-Publica.xlsx)*
- *[Issues](https://github.com/CiudadesAbiertas/vocab-transporte-bicicleta-publica/issues)*

&nbsp;

## DIAGRAMA CONCEPTUAL <a name="id3"></a>

El diagrama muestra las clases y propiedades del vocabulario que representa los convenios adoptados por los ayuntamientos con otras entidades:  
&nbsp;
![Diagrama conceptual](http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica/doc/resources/images/modeloConceptual.png)
&nbsp;



## TABLAS <a name="id4"></a> 

[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### BICI_ESTACION <a name="id5"></a>
&nbsp;

|     Campo                 |     Tipo            |     Ejemplo                     |     Descripción                                                                                                                                                                        |     URL                                                                                                                |
|---------------------------|---------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
|     ikey                  |     VARCHAR(50)     |     1                           |     Identificador de la Tabla (PK).                                                                                                                                                    |                                                                                                                        |
|     id                    |     VARCHAR(50)     |     EST01                       |     El   identificador de una estación de bicicletas.                                                                                                                                  |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier              |
|     portal_id             |     VARCHAR(50)     |                                 |     Id del portal.                                                                                                                                                                     |     http://schema.org/address     .                                                                                    |
|     street_address        |     VARCHAR(200)    |     calle   gran vía            |     La   dirección de la calle.                                                                                                                                                        |     http://schema.org/streetAddress                                                                                    |
|     postal_code           |     VARCHAR(10)     |     28013                       |     El   código postal                                                                                                                                                                 |     http://schema.org/postalCode                                                                                       |
|     equipamiento_id       |     VARCHAR(50)     |                                 |     Identificador   del equipamiento de una estación de bicicletas.                                                                                                                    |     http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento-municipal#id                  |
|     equipamiento_title    |     VARCHAR(200)    |     Estación   gran vía         |     Nombre   del equipamiento de una estación de bicicletas.                                                                                                                           |     http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento-municipal#nombre              |
|     estado_estacion       |     VARCHAR(200)    |     operativa                   |     Cada   estación puede tener estado operativa y no operativa.     URL   SKOS:     http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-estado-estacion    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#estadoEstacion                                   |
|     tipo_equipamiento     |     VARCHAR(200)    |     equipamiento   municipal    |     Tipo de   equipamiento de la estación.     URL   SKOS:     http://vocab.linkeddata.es/datosabiertos/kos/urbanismo-infraestructuras/equipamiento/tipo-equipamiento                  |     http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento-municipal#tipoEquipamiento    |
|     fechaBaja             |                     |     2014-06-23                  |     Fecha de   baja.                                                                                                                                                                   |     http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento-municipal#fechaBaja           |
|     fechaAlta             |                     |     2014-06-23                  |     Fecha de   alta.                                                                                                                                                                   |     http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento-municipal#fechaAlta           |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### BICI_ANCLAJE <a name="id6"></a>
&nbsp;

|     Campo                    |     Tipo            |     Ejemplo    |     Descripción                                                                                                                                                                             |     URL                                                                                                      |
|------------------------------|---------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey                     |     VARCHAR(50)     |     1          |     Identificador de la Tabla (PK).                                                                                                                                                         |                                                                                                              |
|     id                       |     VARCHAR(50)     |     ANC01      |     Identificador   del anclaje de la bicicleta.                                                                                                                                            |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     estado_anclaje           |     VARCHAR(200)    |     libre      |     Cada   anclaje puede tener tener estado libre, ocupado o inactivo.     URL   SKOS:     http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-estado-anclaje    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#estadoAnclaje                          |
|     estacion_bicicleta_id    |     VARCHAR(50)     |     EST01      |     La identificación   de la estación de la bicicleta.     FK a la   tabla de Bici Estación                                                                                                |                                                                                                              |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### BICI_SENSOR <a name="id7"></a>
&nbsp;

|     Campo             |     Tipo            |     Ejemplo              |     Descripción                                                                   |     URL                                                                                                      |
|-----------------------|---------------------|--------------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey              |     VARCHAR(50)     |     1                    |     Identificador de la Tabla (PK).                                               |                                                                                                              |
|     id                |     VARCHAR(50)     |     SEN01                |     Identificador   del sensor de una bicicleta.                                  |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     is_hosted_by      |     VARCHAR(50)     |     EST01                |     Relación   entre un sensor y la plataforma en donde está instalada..          |     http://www.w3.org/ns/sosa/isHostedBy                                                                     |
|     observes_title    |     VARCHAR(100)    |     Anclajes   libres    |     Es el   título o nombre de la propiedad que se está observando.               |                                                                                                              |
|     observes_id       |     VARCHAR(100)    |     anclajesLibres       |     Relación   entre un sensor y una propiedad observable capaz de ser medida.    |     http://www.w3.org/ns/sosa/observes                                                                       |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### BICI_OBSERVACIÓN <a name="id8"></a>
&nbsp;

|     Campo                      |     Tipo             |     Ejemplo                  |     Descripción                                                                  |     URL                                                                                                      |
|--------------------------------|----------------------|------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey                       |     VARCHAR(50)      |     1                        |     Identificador de la Tabla (PK).                                              |                                                                                                              |
|     id                         |     VARCHAR(50)      |     OBS01                    |     Identificador   de una observación.                                          |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     made_by_sensor             |     VARCHAR(50)      |     EST01                    |     Relación   entre una observación y el sensor que ha hecho la observación.    |     http://www.w3.org/ns/sos/madeBySensor                                                                    |
|     observed_property_title    |     VARCHAR(100)     |     Anclajes   libres        |     Es el   título o nombre de la propiedad que se está observando.              |                                                                                                              |
|     observed_property_id       |     VARCHAR(100)     |     anclajesLibres           |     Relación   que une una observación con la propiedad observada.               |     http://www.w3.org/ns/sosa/observedProperty                                                               |
|     result_time                |     datetime         |     2020-01-09   12:14:41    |     Es el   instante en el tiempo en la que se completó la actividad.            |     http://www.w3.org/ns/sos/resultTime                                                                      |
|     has_data_value             |     decimal(12,2)    |     5.00                     |     El valor   de una observación.                                               |     http://www.w3.org/ns/sosa/hasSimpleResult                                                                |
|     quality                    |     varchar(50)      |     número   de anclajes     |     Relación   entre una observación y la calidad del resultado.                 |     http://www.w3.org/ns/ssn/systems/qualityOfObservation                                                    |


[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 
&nbsp;
### BICI_BICICLETA <a name="id9"></a>
&nbsp;

|     Campo        |     Tipo            |     Ejemplo    |     Descripción                                                                                                                                                                                               |     URL                                                                                                      |
|------------------|---------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey         |     VARCHAR(50)     |     1          |     Identificador de la Tabla (PK).                                                                                                                                                                           |                                                                                                              |
|     id           |     VARCHAR(50)     |     BIC01      |     Identificador   de una bicicleta.                                                                                                                                                                         |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     matricula    |     VARCHAR(200)    |     M001       |     Matrícula.                                                                                                                                                                                                |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#matricula                              |
| estado_bicicleta | VARCHAR(200)        | libre          | Cada bicicleta puede tener estado abandonada, libre, en-reparacion, en-reserva, excluida y ocupada. URL SKOS: http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-estado-bicicleta | http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#estadoBicicleta                            |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 

&nbsp;
### BICI_USUARIO <a name="id10"></a>
&nbsp;

|     Campo              |     Tipo            |     Ejemplo    |     Descripción                                  |     URL                                                                                                      |
|------------------------|---------------------|----------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey               |     VARCHAR(50)     |     1          |     Identificador de la Tabla (PK).              |                                                                                                              |
|     id                 |     VARCHAR(50)     |     USU01      |     Identificador   del usuario.                 |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     anio_nacimiento    |     int(4)          |     1981       |     Solamente   el año, no la fecha completa.    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#anioNacimiento                         |
|     sex                |     VARCHAR(200)    |     F          |                                                  |     http://purl.org/linked-data/sdmx/2009/dimension#sex                                                      |


[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 

&nbsp;
### BICI_TRAYECTO <a name="id11"></a>
&nbsp;

|     Campo                            |     Tipo           |     Ejemplo                  |     Descripción                                                                                                                          |     URL                                                                                                      |
|--------------------------------------|--------------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey                             |     VARCHAR(50)    |     1                        |     Identificador de la Tabla (PK).                                                                                                      |                                                                                                              |
|     id                               |     VARCHAR(50)    |     TRA01                    |     Identificador   del trayecto de una bicicleta.                                                                                       |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     start_date                       |     datetime       |     2020-01-09   08:00:00    |     La fecha y   hora de inicio de un item (en formato fecha ISO 8601).                                                                  |     http://schema.org/startDate                                                                              |
|     end_date                         |     datetime       |                              |     La fecha y   hora de finalización de un item (en formato fecha ISO 8601).                                                            |     http://schema.org/endDate                                                                                |
|     usuario_id                       |     VARCHAR(50)    |     USU01                    |     Identificador   de la persona que tiene derecho a usar el sistema de bicicleta pública.                                              |                                                                                                              |
|     bicicleta_id                     |     VARCHAR(50)    |     BIC06                    |     Identificador   de una bicicleta.                                                                                                    |                                                                                                              |
|     estacion_bicicleta_origen_id     |     VARCHAR(50)    |     EST02                    |     Identificador   del enlace entre el trayecto y la estación. Determina cual es la estación de   origen de un trayecto determinado.    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#tieneEstacionOrigen                    |
|     estacion_bicicleta_destino_id    |     VARCHAR(50)    |                              |     Enlace entre   el trayecto y la estación. Determina cual es la estación de origen de un   trayecto determinado.                      |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#tieneEstacionDestino                   |
|     anclaje_origen_id                |     VARCHAR(50)    |     ANC06                    |     Enlace entre   el trayecto y el anclaje. Determina cual es el anclaje de origen de un   trayecto.                                    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#tieneAnclajeOrigen                     |
|     anclaje_destino_id               |     VARCHAR(50)    |                              |     Enlace entre   el trayecto y el anclaje. Determina cual es el anclaje de destino de un   trayecto.                                   |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#tieneAnclajeDestino                    |



[comment]: <!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!> 

&nbsp;
### BICI_PUNTO_PASO <a name="id12"></a>
&nbsp;


|     Campo          |     Tipo                |     Ejemplo                  |     Descripción                                                               |     URL                                                                                                      |
|--------------------|-------------------------|------------------------------|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|     ikey           |     VARCHAR(50)         |     1                        |     Identificador de la Tabla (PK).                                           |                                                                                                              |
|     id             |     VARCHAR(50)         |     PPASO01                  |     Identificador   del punto de paso.                                        |     https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#http://purl.org/dc/terms/identifier    |
|     fecha_paso     |     datetime            |     2020-01-09   07:00:00    |     Fecha de   paso.                                                          |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#fechaPaso                              |
|     trayecto_id    |     VARCHAR(50)         |     TRA04                    |     Espacio que   se recorre para llegar desde un origen hasta un destino.    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#Trayecto                               |
|     orden          |     int(11)             |     1                        |     El número de   orden un punto de paso.                                    |     http://vocab.ciudadesabiertas.es/def/transporte/bicicleta-publica#orden                                  |
|     x_etrs89       |     decimal(13,5)       |     440124.33000             |     Coordenada X   en metros (ETRS89).                                        |     https://datos.ign.es/def/geo_core#xETRS89                                                                |
|     y_etrs89       |     decimal(13,5)       |     4474637.17000            |     Coordenada Y   en metros (ETRS89).                                        |     https://datos.ign.es/def/geo_core#yETRS89                                                                |


&nbsp;



## TAXONOMÍAS SKOS <a name="id13"></a>
&nbsp;

### TIPO-MODELO-BICICLETA <a name="id14"></a>
http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-modelo-bicicleta
&nbsp;
Tesauro que recoge los tipos de modelo de una bicicleta pública.


|     Término      |     Label                                 |
|------------------|-------------------------------------------|
|     electrica    |     La bicicleta es de tipo eléctrica.    |
|     mecanica     |     La bicicleta es de tipo mecánica.     |
&nbsp;

 ### TIPO-ESTADO-ANCLAJE <a name="id15"></a>
 http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-estado-anclaje
 &nbsp;
Tesauro que recoge los tipos de un anclaje de una estación de bicicleta pública.
|     Término      |     Label                                                              |
|------------------|------------------------------------------------------------------------|
|     inactivo     |     El anclaje no está disponible.                                     |
|     libre        |     El anclaje está activo y no está ocupado por ninguna bicicleta.    |
|     ocupado      |     El anclaje está activo y ocupado por una bicicleta.                |
|     reservado    |     El anclaje está activo y está reservado por un usuario.            |
&nbsp;
 
 
 
 ### TIPO-ESTADO-ESTACION <a name="id16"></a>
 http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-estado-estacion
 &nbsp;
Tesauro que recoge los tipos de estado de una estación de bicicleta pública.
|     Término         |     Label                                     |
|---------------------|-----------------------------------------------|
|     no-operativa    |     La estación no está en funcionamiento.    |
|     opertiva        |     La estación está en funcionamiento.       |
&nbsp;


 
 ### TIPO-ESTADO-BICICLETA <a name="id17"></a>
 http://vocab.linkeddata.es/datosabiertos/kos/transporte/bicicleta-publica/tipo-estado-bicicleta
 &nbsp;
Tesauro que recoge los tipos de estado de una bicicleta pública.
|     Término          |     Label                                                                                      |
|----------------------|------------------------------------------------------------------------------------------------|
|     abandonada       |     La bicicleta bien ha sido sustraída o abandonada por un   usuario y no está localizada.    |
|     disponible       |     La bicicleta no está siendo usada por ningún usuario.                                      |
|     en-reparacion    |     La bicicleta no está disponible, está siendo reparada.                                     |
|     en-reserva       |     La bicicleta está preparada para entrar en el sistema, pero   aún no forma parte de él.    |
|     excluida         |     La bicicleta ha dejado de ser parte del sistema.                                           |
|     ocupada          |     La bicicleta está siendo usada por un usuario.                                             |
&nbsp;

 
 ### TIPO-EQUIPAMIENTO <a name="id18"></a>
http://vocab.linkeddata.es/datosabiertos/kos/urbanismo-infraestructuras/equipamiento/tipo-equipamiento
Tesauro para tipos de equipamientos municipales.


&nbsp;




<p float="right" align="center">
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/gobEspana-logo.svg" alt="Logo Gobierno España" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/red-logo.svg" alt="Logo red.es" width="150"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ciudadesInteligentes-logo.svg" alt="Logo CiudadesInteligentes" width="150"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/unionEuropea-logo.svg" alt="Logo UnionEuropea" width="200"/>
</p>


<p float="right" align="center">
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntAcoruna-logo.svg" alt="Logo AyuntACoruña" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntMadrid-logo.svg" alt="Logo Madrid" width="100"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntSantiagoCompostela-logo.svg" alt="Logo Concello Santiago" width="200"/>
<img src="https://ciudadesabiertas.es/assets/img/cabiertas/ayuntZaragoza-logo.svg" alt="Logo Ayun.Zaragoza" width="200"/>
</p>



