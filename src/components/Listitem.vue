<template>
    <li :class="{ active: id === activeId }">
        {{ activeId === id ? msg : '' }}
    </li>
</template>

<style scoped>
.active {
    background-color: yellow;
    /* Cambia esto al estilo que desees para resaltar el elemento activo */
}
</style>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    id: Number,
    msg: String,
    activeId: Number,
});
</script>
