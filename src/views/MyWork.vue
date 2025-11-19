<script setup>
import PageHeader from '@/components/PageHeader.vue'
import portfolioData from '@/data/portfolio.json'
import HeroContainer from '@/components/portfolio/HeroContainer.vue'
</script>

<template>
  <div class="work-page">
    <PageHeader
      title="My Work"
      thumbnail="Banner.jpg"
    />

    <div class="work-categories">
      <h3>Illustrations</h3>
    </div>
  </div>
</template>

<style scoped>

.work-categories {
  text-align: center;
  text-transform: uppercase;
  font-family: Arial, Helvetica, sans-serif;
}

::v-deep(.page-header .header-image) {
  width: 100%;
  max-width: 100%;
  height: 200px;
  display: block;
}
</style>

