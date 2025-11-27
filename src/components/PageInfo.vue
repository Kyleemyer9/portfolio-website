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
    <p v-for="(item, index) in bullets" :key="index" v-html="item"></p>
  </div>
</template>

<style scoped>
.main-content {
  width: 60%;
  margin: 8px auto;
  text-align: center;
  font-size: large;
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.6;
}

.bullet-points {
  width: 60%;
  margin: 32px auto 8px auto;
  text-align: center;
  font-size: small;
  font-family: Arial, Helvetica, sans-serif;
  text-transform: uppercase;
  color: teal;
}
</style>
