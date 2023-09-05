<script setup>
import Listitem from './components/Listitem.vue';
import {ref} from 'vue'

const arr = ref([
  {id:0, msg: 'hello world'},
  {id:1, msg: 'message 2'},
  {id:2, msg: 'learnvue'},
  {id:3, msg: 'next mesage'},
  {id:4, msg: 'yay'},
])

const activeId = ref(0)
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  </header>
  
  <main>
  <button @click="activeId = (activeId + 1)% arr.length">Pulsar</button>
  <ul>
    <Listitem
    v-for="msg in arr"
    :key="msg.id"
    :id="msg.id"
    :msg="msg.msg"
    :active-id="activeId"
    />
  </ul>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
