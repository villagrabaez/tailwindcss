# Tailwind CSS

## Entorno de trabajo

### ¿Qué necesitamos para trabajar con Tailwind?

Primeramente necestamos inicializar el proyecto con npm

    `$ npm init -y`

Además necesitamo instalar algunas librerias

    $ npm install tailwindcss autoprefixer postcss-cli

Inicializamos tailwindcss

    $ npx tailwindcss init

Creamos el archivo de configuracion de postcss

    $ touch postcss.config.js


En el archivo de configuracion de postcss requerimos los plugins a utilizar

    module.exports = {
      plugins: [
        require('tailwindcss'),
        require('autoprefixer')
      ]
    }

Creamos la carpeta en el que guardaremos nuestros estilos: css/tailwind.css y le agreamos las siguientes directivas

    // tailwind.css

    @tailwind base;

    @tailwind components;

    @tailwind utilities;

Instalamos un servidor web

    $ npm install live-server -g

Le indicamos a live-server donde iniciar nuestro sitio web

    $ live-server public

En nuestro archivo package.json creamos un script para producir nuestro css publico

    /*
    *	-o : output
    */

    $ "build": "postcss css/tailwind.css -o public/css/styles.css"

Ejecutamos nuestro script para generar nuestro css publico

    $ npm run build

Generamos la configuracion por defecto de tailwind

    $ npx tailwindcss init tailwind.config.full.js --full

### Librerias para mejorar el proyecto

[Purge css](https://purgecss.com/ "Purge css") nos ayuda a eliminar cosas que no usamos de nuestro css generado por tailwind

[Nanocss](https://cssnano.co/ "Nanocss") nos ayuda a minificar nuestro archivo css generado por tailwind para hacerlo mas liviano y asi mejorar el performance del proyecto.

[Tailwindcss](https://tailwindcss.com/ "Tailwindcss") sitio web oficial de tailwind para ver la documentacion, por cierto esta muy completa.