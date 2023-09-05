<template>
    <!-- Aplicar la clase 'active' al elemento si isActive es verdadero -->
    <li :class="{ active: isActive }">
        {{ msg }}
    </li>
</template>

<style scoped>
.active {
    background-color: yellow;
    /* Cambia este estilo según tus preferencias para resaltar el elemento activo */
}
</style>

<script setup>
import { defineProps } from 'vue';

// Definición de las propiedades que recibe el componente
const props = defineProps({
    msg: String,      // Propiedad para el texto a mostrar
    isActive: Boolean // Propiedad para indicar si el elemento es activo
});
</script>
