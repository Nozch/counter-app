<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue'

const clock = ref(new Date().toLocaleTimeString())

let intervalId: number


onMounted(() => {
    intervalId = 
    setInterval(() => {
        clock.value = new Date().toLocaleTimeString()
    }, 1000)
})

onBeforeUnmount(() => {
    clearInterval(intervalId)
})
</script>
<template>
    <div>{{ clock }}</div>
</template>
