<script setup>
const props = defineProps({
  mainText: {
    type: String,
    required: true
  },
  bullets: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <div class="main-content">
    <p>{{ mainText }}</p>
  </div>

  <div class="bullet-points">
    <p v-for="(item, index) in bullets" :key="index">• {{ item }}</p>
  </div>
</template>

<style scoped>
.main-content {
  border: solid black 1px;
  width: 60%;
  margin: 8px auto;
  text-align: center;
  font-size: large;
  font-family: Arial, Helvetica, sans-serif;
}

.bullet-points {
  border: solid black 1px;
  width: 60%;
  margin: 8px auto;
  text-align: center;
  font-size: medium;
  font-family: Arial, Helvetica, sans-serif;
  text-transform: uppercase;
}
</style>
