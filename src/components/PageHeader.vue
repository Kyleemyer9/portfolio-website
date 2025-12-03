<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true
  },
  thumbnail: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    required: false
  }
})
</script>

<template>
  <div class="page-header">
    <div class="title-row">
      <h2>{{ props.title }}</h2>
      <img
        v-if="props.icon"
        :src="`./src/assets/${props.icon}`"
        alt="icon"
        class="title-icon"
      />
    </div>

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

.title-row {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
}

.page-header h2 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: teal;
}

.title-icon {
  width: 30px;
  height: 30px;
}

.header-image {
  width: 300px;
  height: auto;
  border-radius: 12px;
  border: 1px solid black;
}
</style>
