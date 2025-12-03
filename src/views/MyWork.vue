<script setup>
import PageHeader from '@/components/PageHeader.vue'
import portfolioData from '@/data/portfolio.json'
import HeroContainer from '@/components/portfolio/HeroContainer.vue'

const illustrationItems = [
  portfolioData[0],
  portfolioData[1],
  portfolioData[6],
  portfolioData[8],
]
const posterItems = [
  portfolioData[3],
  portfolioData[11],
  portfolioData[12],
  portfolioData[13],
]
const uiItems = [
  portfolioData[5],
  portfolioData[7],
  portfolioData[14],
  portfolioData[10],
]
const miscItems = [
  portfolioData[2],
  portfolioData[4],
  portfolioData[9],
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

      <h3>UI Design</h3>
      <hero-container :is-responsive="true" :items="uiItems" />

      <h3>Misc. Designs</h3>
      <hero-container :is-responsive="true" :items="miscItems" />
    </div>
  </div>
</template>

<style scoped>

.work-categories {
  text-align: center;
  text-transform: uppercase;
  font-family: Arial, Helvetica, sans-serif;
  color: teal;
}

.work-categories h3 {
  margin-top: 60px;
  margin-bottom: 16px;
}

::v-deep(.page-header .header-image) {
  width: 100%;
  max-width: 100%;
  height: 200px;
  display: block;
}
</style>

