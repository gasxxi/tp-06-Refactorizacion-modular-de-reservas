# Trabajo práctico 06

## Proyecto de partida y cambios
Para este trabajo práctico partí de la entrega del TP 05 de reservas de salas de estudio, donde todo el servidor, los middlewares, las rutas y la memoria estaban concentrados en un solo archivo (`src/index.js`). 
El objetivo principal fue refactorizar la aplicación en una arquitectura modular sin alterar su funcionalidad:
* Aislé la lectura y validación de variables de entorno en `src/configuracion.js`.
* Separé el almacenamiento de datos en memoria en `src/servicios/reservas.js`.
* Creé `src/controladores/reservas.js` para gestionar las peticiones y respuestas HTTP.
* Desacoplé los middlewares de registro e identificación en `src/middleware/solicitudes.js` y los de área y validación en `src/middleware/reservas.js`.
* Definí el router de la entidad en `src/rutas/reservas.js`.
* Separé el armado del pipeline en `src/app.js` de la inicialización y escucha del puerto en `src/index.js`.

## Instalación y ejecución
Para instalar las dependencias necesarias:
```bash
npm install