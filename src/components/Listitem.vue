<script setup>
import { onUpdated } from 'vue';
const props=defineProps({
    id:Number,
    msg: String,
    activeId: Number,
})

onUpdated(() => {
    // will print wheever our component update
    console.log('updating' + props.id)
})
</script>

<template>
    <li>
        <span v-if="id === activeId"></span>
        {{ msg }}
    </li>
</template>