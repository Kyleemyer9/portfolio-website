<script setup>
import { defineProps, computed } from 'vue'
import { RouterLink } from 'vue-router'

const props = defineProps({
  id: Number,
  thumbnail: String,
  title: String,
})

// ✅ ALWAYS works in Vite
const images = import.meta.glob('/src/assets/*.{jpg,png}', {
  eager: true,
  import: 'default',
})

const backgroundImage = computed(() => {
  return images[`/src/assets/${props.thumbnail}`]
})
</script>


<template>
  <RouterLink :to="`/work/${props.id}`" class="hero-wrapper">
    <div
      class="hero"
      :style="{ backgroundImage: `url(${backgroundImage})` }"
    ></div>

    <p class="hero-title">{{ props.title }}</p>
  </RouterLink>
</template>


<style scoped>
.hero-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 300px;
  text-decoration: none;
}

.hero {
  width: 300px;
  height: 250px;
  border: 1px solid black;
  border-radius: 15px;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.hero-title {
  margin-top: 8px;
  text-align: center;
  font-size: small;
  font-family: Arial, Helvetica, sans-serif;
  text-transform: uppercase;
  color: teal;
}
</style>

