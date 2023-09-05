<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  </header>

  <main>
    <button @click="changeActiveItem">Pulsar</button>
    <ul>
      <Listitem v-for="msg in arr" :key="msg.id" :id="msg.id" :msg="msg.msg" :activeId="activeId" />
    </ul>
  </main>
</template>

<script setup>
import Listitem from './components/Listitem.vue';
import { ref } from 'vue';

const arr = ref([
  { id: 0, msg: 'hello world' },
  { id: 1, msg: 'message 2' },
  { id: 2, msg: 'learnvue' },
  { id: 3, msg: 'next message' },
  { id: 4, msg: 'yay' },
]);

const activeId = ref(0);

const changeActiveItem = () => {
  activeId.value = (activeId.value + 1) % arr.value.length;
};
</script>
