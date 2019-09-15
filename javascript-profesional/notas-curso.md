https://augdiaugus.gitbook.io/platzi/escuela-de-javascript/curso-profesional-de-javascript

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