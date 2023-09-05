# vue-project

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
App.vue

App.vue es el componente principal de tu aplicación Vue. En este archivo, defines la estructura principal de tu página web. Aquí tienes una descripción de las partes principales de App.vue:

    <template>: Esta sección contiene la estructura HTML de la página. Aquí defines la cabecera con una imagen de un logo de Vue y un botón llamado "Pulsar". También incluyes una lista (<ul>) que muestra elementos representados por el componente Listitem.

    <script setup>: En esta sección, importas el componente Listitem y otras dependencias necesarias. También defines un array (arr) que contiene objetos con mensajes y un estado activeId que rastrea el índice del elemento activo en la lista. La función changeActiveItem se encarga de cambiar el elemento activo cuando se hace clic en el botón "Pulsar".

    Estilos CSS: En la sección de estilos CSS con el atributo scoped, aplicas estilos al encabezado (header) y defines un estilo especial para resaltar el elemento activo de la lista.

Listitem.vue

Listitem.vue es un componente secundario que se utiliza para representar elementos individuales en la lista de la aplicación. Aquí tienes una descripción de las partes principales de Listitem.vue:

    <template>: Esta sección contiene la estructura HTML para representar un elemento de la lista. Se utiliza un elemento <li> que puede resaltar su fondo en amarillo si isActive es verdadero y muestra el mensaje msg.

    <style scoped>: En la sección de estilos CSS con el atributo scoped, defines un estilo especial llamado .active que cambia el fondo del elemento a amarillo cuando isActive es verdadero. Puedes personalizar este estilo según tus preferencias.

    <script setup>: En esta sección, importas defineProps para definir las propiedades que el componente espera recibir. En este caso, msg es una cadena de texto que representa el mensaje que se mostrará, y isActive es un valor booleano que indica si el elemento debe ser resaltado como activo.

En resumen, App.vue es el componente principal que define la estructura de la página y utiliza el componente Listitem para mostrar elementos individuales en una lista. Listitem.vue es un componente secundario encargado de mostrar cada elemento de la lista y aplicar un estilo especial al elemento activo.
