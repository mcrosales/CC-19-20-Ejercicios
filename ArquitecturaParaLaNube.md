# Ejercicios Arquitecturas Software para la nube .
### Ejercicio 1: 

__Buscar una aplicación de ejemplo, preferiblemente propia, y deducir qué patrón es el que usa. ¿Qué habría que hacer para evolucionar a un patrón tipo microservicios?__

Hace aproximadamente tres años forme parte del equipo de desarrollo de SpecimenSecure, una aplicación para el intercambio de ordenes médicas electrónicas de laboratorios clínicos y patológicos.
Para esta aplicación se utilizó el framework PHP Yii en su versión 2. Este framework utiliza por defecto una arquitectura de 3 capas Modelo-Vista-Conrolador. Para llevar esta apliacion a micorservicios, 
seria necesario separar la alta dependencia entre la vista y la logica de negocio, transformando por ejemplo grupos de controladores en microservicios REST.
### Ejercicio 2: 

__En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?__
 
De hecho se usan varios lenguajes, principalmente javascript en la capa de Vista para tratar de lograr un enfoque cercano a una Sinle Page Application,
 lo cual hubiese sido mas factible utilzando Angular o React en detrimento de jQuery. Del lado del controlador, si estuviesen separadas las funcionalidades en microservicios, 
 se podrian haber utilizados librerias escritas en otros lenguajes para el tratamiento de imágenes. Al utilzar APIs REST y por ende documentos JSON, 
 hubiera sido interesante medir el rendimiento de MongoDB como alternativa a PostgreSQL.