<script setup>
import PageHeader from '@/components/PageHeader.vue'
</script>

<template>
  <div class="workPage">
    <PageHeader
      title="My Work"
      thumbnail="Banner.jpg"
    />
  </div>
</template>

<style scoped>

::v-deep(.page-header .header-image) {
  width: 80%;
  max-width: 100%;
  height: 200px;
  display: block;
}
</style>
