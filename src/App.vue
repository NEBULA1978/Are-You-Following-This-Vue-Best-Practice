<template>
  <header>
    <!-- Logo de Vue -->
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  </header>

  <main>
    <!-- Botón para cambiar el elemento activo -->
    <button @click="changeActiveItem">Pulsar</button>
    <ul>
      <!-- Itera a través de los elementos y muestra cada uno con su estado activo -->
      <Listitem v-for="msg in arr" :key="msg.id" :msg="msg.msg" :isActive="activeId === msg.id" />
    </ul>
  </main>
</template>

<script setup>
import Listitem from './components/Listitem.vue';
import { ref } from 'vue';

// Array de mensajes
const arr = ref([
  { id: 0, msg: 'hello world' },
  { id: 1, msg: 'message 2' },
  { id: 2, msg: 'learnvue' },
  { id: 3, msg: 'next message' },
  { id: 4, msg: 'yay' },
]);

// Estado del elemento activo
const activeId = ref(0);

// Función para cambiar el elemento activo
const changeActiveItem = () => {
  activeId.value = (activeId.value + 1) % arr.value.length;
};
</script>
