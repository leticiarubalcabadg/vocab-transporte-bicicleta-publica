# transporte-bicicleta-publica
Este vocabulario está siendo desarrollado en el contexto de la actuación sobre datos abiertos del proyecto [Plataforma de Gobierno Abierto, Colaborativa e Interoperable](http://www.red.es/redes/es/que-hacemos/ciudades-inteligentes/proyectos-en-ciudades), de la [II Convocatoria de Ciudades Inteligentes](https://perfilcontratante.red.es/perfilcontratante/busqueda/DetalleLicitacionesDefault.action?idLicitacion=6707&visualizar=0) del [Ministerio de Economía](http://www.mineco.gob.es/) y Empresa lanzada a través de la [Entidad Pública Empresarial Red.es](http://www.red.es/) adscrita a la [Secretaría de Estado de Avance Digital de dicho Ministerio](http://www.mineco.gob.es/portal/site/mineco/avancedigital).

## Propósito y alcance del vocabulario
El propósito y alcance de este vocabulario está motivado por la definición proporcionada en la guía publicada por el Grupo de Trabajo de Datos Abiertos creado por la FEMP: ["Datos Abiertos: Guía estratégica para su puesta en marcha. Conjuntos de datos mínimos a publicar"](http://femp.femp.es/files/3580-1617-fichero/Gu%C3%ADa%20Datos%20Abiertos.pdf). Según este documento, el propósito de este vocabulario es representar la información relativa a la bicicleta pública tanto en la parte relacionada a los trayectos realizados por los usuarios como a las estaciones y los anclajes que las componen. Por lo tanto, el alcance del vocabulario se centra en cubrir la representación de las estaciones, sus anclajes, el estado del material, tanto bicicletas como estaciones y, por último, los recorridos realizados por los usuarios.

## Desarrollo del vocabulario
El material generado en las diferentes actividades ejecutadas durante el desarrollo del vocabulario, casos de uso, historias de usuario, glosario de términos, etc., se encuentra disponible en la [Wiki del Vocabulario](https://github.com/CiudadesAbiertas/vocab-transporte-bicicleta-publica/wiki).

También se ha propuesto un modelo relacional tipo, que está  documentado *[aquí](relational_model/README.md)*, que ha sido utilizado para la generación de  una API REST relacionada con este vocabulario, en el contexto del  proyecto Ciudades Abiertas. Este modelo relacional no está  completamente normalizado, para facilitar algunos procesos de  Extracción, Transformación y Carga (ETLs, por sus siglas en inglés),  habituales en muchos portales de datos abiertos, y no es normativo,  por lo que cualquier organización que adopte este vocabulario para la  publicación de sus datos abiertos puede proponer variaciones siempre  que se respete la forma de exportación a RDF de los datos  correspondientes.


## Mantenimiento
Para gestionar aquellas incidencias o mejoras sugeridas con respecto al vocabulario te recomendamos seguir las guías proporcionadas en [Gestión de Issues](https://github.com/CiudadesAbiertas/vocab-transporte-bicicleta-publica/wiki/Gesti%C3%B3n-de-issues)

## Ejemplos

Algunas [consultas](https://github.com/CiudadesAbiertas/vocab-transporte-bicicleta-publica/blob/master/examples/queries.md) a realizar en un SPARQL endpoint de pruebas se han habilitado para ejemplificar su funcionamiento.
