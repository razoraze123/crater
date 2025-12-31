<template>
  <component :is="heroIcons[name]" v-if="isLoaded" class="h-5 w-5" />
</template>

<script setup>
import { ref, onMounted } from 'vue'
import heroIcons from './icons-map.js'

const isLoaded = ref(false)

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
})

onMounted(() => {
  isLoaded.value = true
})
</script>
