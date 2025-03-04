<template><div><h1 id="tutorial-para-la-configuracion-manual-de-vuepress-2-0" tabindex="-1"><a class="header-anchor" href="#tutorial-para-la-configuracion-manual-de-vuepress-2-0"><span>Tutorial para la configuración Manual de VuePress 2.0</span></a></h1>
<p>Este proyecto está configurado manualmente siguiendo la <a href="https://vuepress.vuejs.org/guide/getting-started.html#project-setup" target="_blank" rel="noopener noreferrer">guía oficial de VuePress</a>.</p>
<h2 id="requisitos-previos" tabindex="-1"><a class="header-anchor" href="#requisitos-previos"><span>Requisitos previos</span></a></h2>
<p>Debemos tener instalado previamente Node.js y yarn.</p>
<ul>
<li><a href="https://nodejs.org/en/" target="_blank" rel="noopener noreferrer">Node.js</a> versión 16+</li>
<li><a href="https://yarnpkg.com/getting-started/install" target="_blank" rel="noopener noreferrer">Yarn</a></li>
</ul>
<p>Comprobamos si están instalados y su versión con:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token function">yarn</span> <span class="token parameter variable">--version</span></span>
<span class="line"><span class="token function">node</span> <span class="token parameter variable">--version</span></span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div><div class="line-number"></div></div></div><p><img src="/imagenes/Imagen1.png" alt="Descripción de la imagen"></p>
<h2 id="instalacion" tabindex="-1"><a class="header-anchor" href="#instalacion"><span>Instalación</span></a></h2>
<h3 id="paso-1-crear-y-configurar-tu-proyecto" tabindex="-1"><a class="header-anchor" href="#paso-1-crear-y-configurar-tu-proyecto"><span>Paso 1: Crear y configurar tu proyecto</span></a></h3>
<p>Primero, crea un directorio para tu proyecto y navega hacia él:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token function">mkdir</span> proyecto</span>
<span class="line"><span class="token builtin class-name">cd</span> proyecto</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div><div class="line-number"></div></div></div><p><img src="/imagenes/Imagen2.png" alt="Descripción de la imagen"></p>
<p>Inicializa el proyecto con yarn:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token function">yarn</span> init</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div></div></div><p><img src="/imagenes/Imagen3.png" alt="Descripción de la imagen"></p>
<p>Completa la información solicitada o presiona Enter para aceptar los valores predeterminados.</p>
<h3 id="paso-2-instalar-vuepress-y-sus-dependencias" tabindex="-1"><a class="header-anchor" href="#paso-2-instalar-vuepress-y-sus-dependencias"><span>Paso 2: Instalar VuePress y sus dependencias</span></a></h3>
<p>Instala VuePress 2.0 y sus dependencias como dependencias de desarrollo:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token comment"># install vuepress</span></span>
<span class="line"><span class="token function">yarn</span> <span class="token function">add</span> <span class="token parameter variable">-D</span> vuepress@next</span>
<span class="line"><span class="token comment"># install bundler and theme</span></span>
<span class="line"><span class="token function">yarn</span> <span class="token function">add</span> <span class="token parameter variable">-D</span> @vuepress/bundler-vite@next @vuepress/theme-default@next</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><img src="/imagenes/Imagen4.png" alt="Descripción de la imagen"></p>
<h3 id="paso-3-crear-la-estructura-de-directorios" tabindex="-1"><a class="header-anchor" href="#paso-3-crear-la-estructura-de-directorios"><span>Paso 3: Crear la estructura de directorios</span></a></h3>
<p>Crea la siguiente estructura básica para tu proyecto:</p>
<div class="language-text line-numbers-mode" data-highlighter="prismjs" data-ext="text" data-title="text"><pre v-pre><code><span class="line">mi-proyecto-vuepress</span>
<span class="line">├── docs</span>
<span class="line">│   ├── .vuepress</span>
<span class="line">│   │   └── config.ts</span>
<span class="line">│   └── README.md</span>
<span class="line">└── package.json</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><img src="/imagenes/Imagen5.png" alt="Descripción de la imagen"></p>
<h3 id="paso-4-configurar-el-archivo-config-js" tabindex="-1"><a class="header-anchor" href="#paso-4-configurar-el-archivo-config-js"><span>Paso 4: Configurar el archivo config.js</span></a></h3>
<p>A partir de ahora vamos a abrir el proyecto en VSCode y trabajar desde allí.</p>
<p>Edita el archivo <code v-pre>docs/.vuepress/config.js</code>:</p>
<p><img src="/imagenes/Imagen6.png" alt="Descripción de la imagen"></p>
<h3 id="paso-5-crear-tu-primera-pagina" tabindex="-1"><a class="header-anchor" href="#paso-5-crear-tu-primera-pagina"><span>Paso 5: Crear tu primera página</span></a></h3>
<p>Edita el archivo <code v-pre>docs/README.md</code> y añade algún contenido:</p>
<p><img src="/imagenes/Imagen7.png" alt="Descripción de la imagen"></p>
<h3 id="paso-6-arrancar-el-dev-server" tabindex="-1"><a class="header-anchor" href="#paso-6-arrancar-el-dev-server"><span>Paso 6: Arrancar el Dev Server</span></a></h3>
<p>Antes de arrancar el Dev Server añadimos scripts a package.json</p>
<p><img src="/imagenes/Imagen8.png" alt="Descripción de la imagen"></p>
<p>Después arrancamos el servidor en la terminal con:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token function">yarn</span> docs:dev</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div></div></div><p><img src="/imagenes/Imagen9.png" alt="Descripción de la imagen"></p>
<p>Ahora puedes acceder a tu sitio en <code v-pre>http://localhost:8080</code>.</p>
<p><img src="/imagenes/Imagen10.png" alt="Descripción de la imagen"></p>
<h3 id="paso-7-construir-para-produccion" tabindex="-1"><a class="header-anchor" href="#paso-7-construir-para-produccion"><span>Paso 7: Construir para producción</span></a></h3>
<p>Cuando estés listo para desplegar tu sitio:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token function">yarn</span> docs:build</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div></div></div><p>Esto generará archivos estáticos en <code v-pre>docs/.vuepress/dist/</code> que podrás desplegar en cualquier servicio de hosting.</p>
<h3 id="paso-8-anadir-contenido" tabindex="-1"><a class="header-anchor" href="#paso-8-anadir-contenido"><span>Paso 8: Añadir contenido</span></a></h3>
<p>Ahora puedes ir al archivo README.md y modificarlo para darle contenido a tu página. El lenguaje empleado es Markdown, por lo que tienes que seguir sus reglas.</p>
<p><img src="/imagenes/Imagen10.5.png" alt="Descripción de la imagen"></p>
<h2 id="cambiar-el-tema" tabindex="-1"><a class="header-anchor" href="#cambiar-el-tema"><span>Cambiar el tema</span></a></h2>
<p>VuePress 2.0 permite cambiar entre temas disponibles o crear tus propios temas. Aquí te muestro cómo cambiar a algunos temas populares:</p>
<h3 id="opcion-1-personalizar-el-tema-por-defecto" tabindex="-1"><a class="header-anchor" href="#opcion-1-personalizar-el-tema-por-defecto"><span>Opción 1: Personalizar el tema por defecto</span></a></h3>
<p>Puedes personalizar el tema por defecto ajustando su configuración:</p>
<p><img src="/imagenes/Imagen11.png" alt="Descripción de la imagen"></p>
<h3 id="opcion-2-instalar-y-usar-un-tema-de-la-comunidad" tabindex="-1"><a class="header-anchor" href="#opcion-2-instalar-y-usar-un-tema-de-la-comunidad"><span>Opción 2: Instalar y usar un tema de la comunidad</span></a></h3>
<p>Primero, instala el tema que deseas utilizar:</p>
<div class="language-bash line-numbers-mode" data-highlighter="prismjs" data-ext="sh" data-title="sh"><pre v-pre><code><span class="line"><span class="token function">yarn</span> <span class="token function">add</span> <span class="token parameter variable">-D</span> vuepress-theme-hope</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div></div></div><p>Luego, configúralo en tu archivo <code v-pre>config.ts</code>:</p>
<div class="language-typescript line-numbers-mode" data-highlighter="prismjs" data-ext="ts" data-title="ts"><pre v-pre><code><span class="line"><span class="token keyword">import</span> <span class="token punctuation">{</span> viteBundler <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'@vuepress/bundler-vite'</span></span>
<span class="line"><span class="token keyword">import</span> <span class="token punctuation">{</span> hopeTheme <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'vuepress-theme-hope'</span></span>
<span class="line"><span class="token keyword">import</span> <span class="token punctuation">{</span> defineUserConfig <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'vuepress'</span></span>
<span class="line"></span>
<span class="line"><span class="token keyword">export</span> <span class="token keyword">default</span> <span class="token function">defineUserConfig</span><span class="token punctuation">(</span><span class="token punctuation">{</span></span>
<span class="line">  bundler<span class="token operator">:</span> <span class="token function">viteBundler</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">,</span></span>
<span class="line">  theme<span class="token operator">:</span> <span class="token function">hopeTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span></span>
<span class="line">    <span class="token comment">// configuración específica del tema hope</span></span>
<span class="line">    hostname<span class="token operator">:</span> <span class="token string">'https://tu-sitio.com'</span><span class="token punctuation">,</span></span>
<span class="line">    author<span class="token operator">:</span> <span class="token punctuation">{</span></span>
<span class="line">      name<span class="token operator">:</span> <span class="token string">'Tu Nombre'</span><span class="token punctuation">,</span></span>
<span class="line">      url<span class="token operator">:</span> <span class="token string">'https://github.com/tu-usuario'</span><span class="token punctuation">,</span></span>
<span class="line">    <span class="token punctuation">}</span><span class="token punctuation">,</span></span>
<span class="line">    <span class="token comment">// más opciones...</span></span>
<span class="line">  <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">,</span></span>
<span class="line"><span class="token punctuation">}</span><span class="token punctuation">)</span></span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="anadir-contenido-multimedia" tabindex="-1"><a class="header-anchor" href="#anadir-contenido-multimedia"><span>Añadir contenido multimedia</span></a></h2>
<p>VuePress facilita la incorporación de imágenes, videos y otros elementos multimedia en tus documentos markdown. A continuación vemos cómo hacerlo:</p>
<h3 id="configuracion-del-directorio-publico" tabindex="-1"><a class="header-anchor" href="#configuracion-del-directorio-publico"><span>Configuración del directorio público</span></a></h3>
<p>Primero, crea un directorio <code v-pre>public</code> dentro de <code v-pre>.vuepress</code> para almacenar tus archivos multimedia:</p>
<div class="language-text line-numbers-mode" data-highlighter="prismjs" data-ext="text" data-title="text"><pre v-pre><code><span class="line">mkdir -p docs/.vuepress/public/imagenes</span>
<span class="line">mkdir -p docs/.vuepress/public/videos</span>
<span class="line"></span></code></pre>
<div class="line-numbers" aria-hidden="true" style="counter-reset:line-number 0"><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="anadir-imagenes" tabindex="-1"><a class="header-anchor" href="#anadir-imagenes"><span>Añadir imágenes</span></a></h3>
<ol>
<li>Coloca tus imágenes en el directorio <code v-pre>docs/.vuepress/public/imagenes/</code></li>
<li>En tus archivos markdown, referencia las imágenes con la ruta <code v-pre>/imagenes/nombre-de-la-imagen.png</code></li>
</ol>
<h3 id="anadir-videos" tabindex="-1"><a class="header-anchor" href="#anadir-videos"><span>Añadir videos</span></a></h3>
<h4 id="opcion-1-videos-alojados-localmente" tabindex="-1"><a class="header-anchor" href="#opcion-1-videos-alojados-localmente"><span>Opción 1: Videos alojados localmente</span></a></h4>
<ol>
<li>Coloca tus videos en el directorio <code v-pre>docs/.vuepress/public/videos/</code></li>
<li>Usa la etiqueta HTML <code v-pre>&lt;video&gt;</code> para mostrarlos:</li>
</ol>
<h2 id="video-local" tabindex="-1"><a class="header-anchor" href="#video-local"><span>Video local</span></a></h2>
<h2 id="my-video" tabindex="-1"><a class="header-anchor" href="#my-video"><span>My Video</span></a></h2>
<video controls width="600">
  <source src="/videos/video2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
</div></template>


