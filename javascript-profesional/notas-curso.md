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


 ## Publicar en npm

 ### Paso 1: npm actualizado

Tener npm instalado y actualizado en tu sistema. Si no está actualizado ejecuta:

```bash
npm install npm@latest -g
```

Fuente: [https://docs.npmjs.com/getting-started/installing-node](https://docs.npmjs.com/getting-started/installing-node)

### Paso 2: github

Tener tu proyecto en Github. No obligatorio pero recomendable. Recuerda que solo puedes publicar gratis paquetes públicos. Para paquetes privados deberás sacar la tarjeta de crédito.

### Paso 3: package.json

Tu proyecto debe tener un archivo `package.json` en el directorio raíz. Si no lo tuviera, ejecuta `npm init` desde la consola y sigue los pasos.

### Paso 4: tu cuenta en npmjs.com

Ve a [npmjs.com](https://www.npmjs.com/) y crea una cuenta. Una vez creada tu cuenta no encontrarás ningún botón de subir proyecto, así que no pierdas tiempo buscándolo \(como yo\).

### Paso 5: publicar el proyecto

Ahora que tienes tu cuenta, ve a tu proyecto en local con la terminal y ejecuta:

```bash
npm login
// ingresa tus datos de usuario y contraseña de npmjs.com
```

Una vez que has iniciado sesión es tan simple como ejecutar:

```bash
npm publish
```
### convertir los archivos TypeScript .ts  a .js 
`npm i -D typescript`
- vamos a Packege.jon y modificamos el script 

```
{
  "name": "@ruber_infinity/platzimediaplayer",
  "version": "1.0.0",
  "main": "lib/MediaPlayer.js",
  "scripts": {
    "build": "tsc src/**/*.ts src/plugins/*.ts src/plugins/**/*.ts --outDir lib",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "ruber",
  "license": "ISC",
  "dependencies": {},
  "devDependencies": {
    "typescript": "^3.6.3"
  },
  "description": ""
}
```
crear en la carpeta MediaPlayer el `.gitingnore` y añandimos los siguiente:
`
node_modules
lib
'
### ejecutamos el comando 

`npm run build`

### chequeamos que estemos logueados en Npm con:

`npm whoami`
» ruber_infinity

### luego publicamos nuestro proyecto a npm publico:

`npm publish --access=public`
```JavaScript
npm notice 📦  @ruber_infinity/platzimediaplayer@1.0.0
npm notice === Tarball Contents === 
npm notice 16B   .gitingnore                
npm notice 4.3kB lib/plugins/Ads/Ads.js     
npm notice 1.3kB lib/plugins/AutoPause.js   
npm notice 338B  lib/plugins/AutoPlay.js    
npm notice 1.8kB lib/plugins/Ads/index.js   
npm notice 1.4kB lib/MediaPlayer.js  
npm notice === Tarball Details === 
npm notice name:          @ruber_infinity/platzimediaplayer       
npm notice version:       1.0.0                                   
npm notice package size:  4.5 kB                                  
npm notice unpacked size: 23.3 kB                                 
npm notice shasum:        74a35641ef0ff346af16ffee24c17e2607ad9870
npm notice integrity:     sha512-7yQyv8F507Bmh[...]Nm5GUwptlSQAA==
npm notice total files:   16                                      
npm notice 
`+ @ruber_infinity/platzimediaplayer@1.0.0`

```
### Nos pasamos a la carpeta de 'website' 
Por que en index.js esta llamando a Mediaplayer y no estan;  toca instalarlos con Npm para que queden como parte de nuestras dependencias con el siguiente comando

`npm install @ruber_infinity/platzimediaplayer` 

=> npm install @[tu usuario_npm]/platzimediaplayer y cuando termine no colocar las dependencias en `packege.json`

```JavaScript
"name": "platzi-media-player",
          "version": "1.0.0",
          "description": "Proyecto del Curso Profesional de JavaScript de la Escuela de JavaScript de Platzi.",
          "license": "MIT",
          "author": "César Augusto Barco <augustopayza@gmail.com>",
          "keywords": [
                    "platzi"
          ],
          "scripts": {
                    "start": "parcel index.html ejercicios/index.html ejercicios/**/*.html"
          },
          "devDependencies": {
                    "eslint": "^6.4.0",
                    "parcel-bundler": "^1.12.3",
                    "typescript": "^3.6.3"
          },
          "browserslist": [
                    "last 1 chrome version"
          ],
          "dependencies": {
                    "@ruber_infinity/platzimediaplayer": "^1.0.0"
          }
```
### Luego vamos a modificar la ruta de nuestros archivos en el index.js

`import MediaPlayer from "./MediaPlayer";`
`import AutoPlay from "../../mediaplayer/src/plugins/AutoPlay";`
`import AutoPause from "../../mediaplayer/src/plugins/AutoPause";`
`import Ads from "../../mediaplayer/src/plugins/Ads";`  
los modificamos a :
```
import MediaPlayer from "@ruber_infinity/platzimediaplayer";
import AutoPlay from "@ruber_infinity/platzimediaplayer/lib/plugins/AutoPlay";
import AutoPause from "@ruber_infinity/platzimediaplayer/lib/plugins/AutoPause";
import Ads from "@ruber_infinity/platzimediaplayer/lib/plugins/Ads";  

```
### luego instalamos todos los modulos  con 
`npm i`

### ya podemos correr el servidor con: 
`npm run start`