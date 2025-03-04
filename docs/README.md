# Tutorial para la configuración Manual de VuePress 2.0

Este proyecto está configurado manualmente siguiendo la [guía oficial de VuePress](https://vuepress.vuejs.org/guide/getting-started.html#project-setup).

## Requisitos previos

Debemos tener instalado previamente Node.js y yarn. 

- [Node.js](https://nodejs.org/en/) versión 16+
- [Yarn](https://yarnpkg.com/getting-started/install)

Comprobamos si están instalados y su versión con:

```bash
yarn --version
node --version
```
![Descripción de la imagen](/imagenes/Imagen1.png)


## Instalación

### Paso 1: Crear y configurar tu proyecto

Primero, crea un directorio para tu proyecto y navega hacia él:

```bash
mkdir proyecto
cd proyecto
```
![Descripción de la imagen](/imagenes/Imagen2.png)

Inicializa el proyecto con yarn:

```bash
yarn init
```

![Descripción de la imagen](/imagenes/Imagen3.png)

Completa la información solicitada o presiona Enter para aceptar los valores predeterminados. 

### Paso 2: Instalar VuePress y sus dependencias

Instala VuePress 2.0 y sus dependencias como dependencias de desarrollo:

```bash
# install vuepress
yarn add -D vuepress@next
# install bundler and theme
yarn add -D @vuepress/bundler-vite@next @vuepress/theme-default@next
```
![Descripción de la imagen](/imagenes/Imagen4.png)

### Paso 3: Crear la estructura de directorios

Crea la siguiente estructura básica para tu proyecto:

```
mi-proyecto-vuepress
├── docs
│   ├── .vuepress
│   │   └── config.ts
│   └── README.md
└── package.json
```



![Descripción de la imagen](/imagenes/Imagen5.png)

### Paso 4: Configurar el archivo config.js

A partir de ahora vamos a abrir el proyecto en VSCode y trabajar desde allí.

Edita el archivo `docs/.vuepress/config.js`:

![Descripción de la imagen](/imagenes/Imagen6.png)


### Paso 5: Crear tu primera página

Edita el archivo `docs/README.md` y añade algún contenido:

![Descripción de la imagen](/imagenes/Imagen7.png)



### Paso 6: Arrancar el Dev Server

Antes de arrancar el Dev Server añadimos scripts a package.json

![Descripción de la imagen](/imagenes/Imagen8.png)

Después arrancamos el servidor en la terminal con:

```bash
yarn docs:dev
```

![Descripción de la imagen](/imagenes/Imagen9.png)

Ahora puedes acceder a tu sitio en `http://localhost:8080`.

![Descripción de la imagen](/imagenes/Imagen10.png)


### Paso 7: Construir para producción

Cuando estés listo para desplegar tu sitio:

```bash
yarn docs:build
```

Esto generará archivos estáticos en `docs/.vuepress/dist/` que podrás desplegar en cualquier servicio de hosting.

### Paso 8: Añadir contenido

Ahora puedes ir al archivo README.md y modificarlo para darle contenido a tu página. El lenguaje empleado es Markdown, por lo que tienes que seguir sus reglas.

![Descripción de la imagen](/imagenes/Imagen10.5.png)

## Cambiar el tema

VuePress 2.0 permite cambiar entre temas disponibles o crear tus propios temas. Aquí te muestro cómo cambiar a algunos temas populares:

### Opción 1: Personalizar el tema por defecto

Puedes personalizar el tema por defecto ajustando su configuración:

![Descripción de la imagen](/imagenes/Imagen11.png)


### Opción 2: Instalar y usar un tema de la comunidad

Primero, instala el tema que deseas utilizar:

```bash
yarn add -D vuepress-theme-hope
```

Luego, configúralo en tu archivo `config.ts`:

```typescript
import { viteBundler } from '@vuepress/bundler-vite'
import { hopeTheme } from 'vuepress-theme-hope'
import { defineUserConfig } from 'vuepress'

export default defineUserConfig({
  bundler: viteBundler(),
  theme: hopeTheme({
    // configuración específica del tema hope
    hostname: 'https://tu-sitio.com',
    author: {
      name: 'Tu Nombre',
      url: 'https://github.com/tu-usuario',
    },
    // más opciones...
  }),
})
```
## Añadir contenido multimedia

VuePress facilita la incorporación de imágenes, videos y otros elementos multimedia en tus documentos markdown. A continuación vemos cómo hacerlo:

### Configuración del directorio público

Primero, crea un directorio `public` dentro de `.vuepress` para almacenar tus archivos multimedia:



```
mkdir -p docs/.vuepress/public/imagenes
mkdir -p docs/.vuepress/public/videos
```

### Añadir imágenes

1. Coloca tus imágenes en el directorio `docs/.vuepress/public/imagenes/`
2. En tus archivos markdown, referencia las imágenes con la ruta `/imagenes/nombre-de-la-imagen.png`

### Añadir videos

#### Opción 1: Videos alojados localmente

1. Coloca tus videos en el directorio `docs/.vuepress/public/videos/`
2. Usa la etiqueta HTML `<video>` para mostrarlos:





