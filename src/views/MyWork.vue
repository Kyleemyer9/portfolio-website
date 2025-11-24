<script setup>
import PageHeader from '@/components/PageHeader.vue'
import portfolioData from '@/data/portfolio.json'
import HeroContainer from '@/components/portfolio/HeroContainer.vue'

const illustrationItems = [
  portfolioData[0],
  portfolioData[1],
]
const posterItems = [
  portfolioData[3],
  portfolioData[7],
]
const brandItems = [
  portfolioData[2],
  portfolioData[4],
]
const uiItems = [
  portfolioData[5],
  portfolioData[7],
]
</script>

<template>
  <div class="work-page">
    <PageHeader
      title="My Work"
      thumbnail="Banner.jpg"
    />

    <div class="work-categories">
      <h3>Illustrations</h3>
      <hero-container :is-responsive="true" :items="illustrationItems" />

      <h3>Posters / Covers</h3>
      <hero-container :is-responsive="true" :items="posterItems" />

      <h3>Brand Identities</h3>
      <hero-container :is-responsive="true" :items="brandItems" />

      <h3>UI Design</h3>
      <hero-container :is-responsive="true" :items="uiItems" />
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

