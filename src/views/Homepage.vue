<script setup>
import portfolioData from '@/data/portfolio.json'
import HeroContainer from '@/components/portfolio/HeroContainer.vue'
import PageHeader from '@/components/PageHeader.vue'

const featuredItems = [
  portfolioData[0],
  portfolioData[1],
  portfolioData[2],
  portfolioData[3],
  portfolioData[4],
  portfolioData[5]
]
</script>

<template>
  <div class="homepage">

    <PageHeader
      title="Kylee Myer"
      thumbnail="your-image.jpg"
    />

    <h2>Featured Works</h2>
    <hero-container :is-responsive="true" :items="featuredItems" />
  </div>
</template>

<style scoped>
.homepage {
  text-align: center;
}
</style>
