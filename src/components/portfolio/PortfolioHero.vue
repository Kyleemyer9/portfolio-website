<script setup >
const props = defineProps({
  thumbnail: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="hero"> :style="`background-image: url(./src/assets/${props.thumbnail})`">
    <img :src="'./src/assets/' + props.thumbnail" />
    <div class="opaque-footer">{{ props.title }}</div>
  </div>
</template>

<style scoped>
.hero {
  border: 1px solid black;
  border-radius: 15px;
  min-height: 200px;
  width: 300px;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;

  .opaque-footer {
    background-color: black;
    color: white;
    padding: 16px;
    text-transform: uppercase;
    opacity: 0.7;
    border-radius: 0 0 15px 15px;
  }
}
</style>
