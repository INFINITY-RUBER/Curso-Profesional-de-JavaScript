https://augdiaugus.gitbook.io/platzi/escuela-de-javascript/curso-profesional-de-javascript

https://augdiaugus.gitbook.io/recoleccion-de-notas-publicas/escuela-de-javascript/curso-profesional-de-javascript

Primer paso
Crearemos nuestros primeros archivos usando `npm init -y`, donde -y es una bandera que le dicta a npm que le diga sí a todas las preguntas que haga.
`npm init -y`
Esto nos creará un archivo package.json que lo sustituiremos por el siguiente:
```
{
"name": "platzi-media-player",
"version": "1.0.0",
"description": "Proyecto del Curso Profesional de JavaScript de la Escuela de JavaScript de Platzi.",
"license": "MIT",
"author": "César Augusto Barco <augustopayza@gmail.com>",
"keywords": [
                "platzi"
        ],
"scripts": {
                "start": "live-server"
        },
"devDependencies": {
        "live-server": "^1.2.1"
    }
}
```

Una vez tengamos todo esto listo vamos a proceder a instalar nuestro live-server para empezar a trabajar. Para instalar esto vamos a usar el siguiente comando:
 `npm i -D live-server` 
donde i significa install y la bandera -D develoment, esto quiere decir que no lo vamos a usar en producción. Una vez instalado ya lo podremos usar con el package.json que dejé arriba. Lo usaremos con el comando start que llamará a su vez a live-server.
`npm start `
## Documentacion  HTMLMediaEleme
https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement

## Introducción TypeScript 
TypeScript es un superset de JavaScript que añade tipos a nuestras variables ayudando así a la detección de errores de forma temprana y mejorando el autocompletado.
Los navegadores no entienden TypeScript así que lo vamos a transpilar a JavaScript usando Parcel.
`npm install -D parcel-bundler `
quitamos en antiguo server
`npm rm live-server` 
y ahora corremos el nuevo server:
`npm start`
- luego de crear configurar la ruta de TYPESCRIPT  detenemos el server y  borramos cache 
 `rm -rf .cache dist`