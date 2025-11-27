<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true
  },
  thumbnail: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="page-header">
    <h2>{{ props.title }}</h2>

    <img
      :src="`./src/assets/${props.thumbnail}`"
      alt="Page Header Image"
      class="header-image"
    />
  </div>
</template>

<style scoped>
.page-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin: 2rem 0;
}

.page-header h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: teal;
}

.header-image {
  width: 300px;
  height: auto;
  border-radius: 12px;
}
</style>
