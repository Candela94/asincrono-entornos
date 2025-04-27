# asincrono-entornos


## qué son 

configuraciones especificas que permiten que ciertas apps se puedan ejecutar en distintos contextos. Nos permiten ajustar ciertas variables y comportamientos de una app

Tipos: 

- de desarrollo: generar pequeñas variables para nuestro ordena 
- pruebas: frameworks
- producción: app publicada en internet 

## .env
Guardamos datos, almacenamos variables o constantes que tiene info sensible y que no deben aparecer en nuestro código. Son variables invisibles. 
- usuario contraseñas..
- apis externas claves 
- configuracione  de puertos 



## Vite 
Tiene  dotenv instalado por defecto

1. creamos archivos .env y .env.production
2. .env dentro de gitignore
3. Añadimos info siempre con VITE_(...) siempre en mayúscula. 
4. En App la importamos 

```js


const {VITE_HOST} = import.meta.env



```

creamos .env 
definimos VITE_API = "http://localhost:3000"
definimos VITE_USERS = (fetch, luego lo sustituimos por {VITE_USERS = import.meta...})
en el fetch en App.js 


## Express

Varias formas de usar los entornos.
- Forma nativa (sin archivos)
- Usando dotenv

1. Definimos en config
2. importamos en index.js
3. process.env.HOST



en index.js definimos const PORT = process.env.PORT || 3000



