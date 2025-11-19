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
      thumbnail="Banner.jpg"
    />
<div class="featured-works">
  <h3>Featured Works</h3>
</div>
    <hero-container :is-responsive="true" :items="featuredItems" />
  </div>
</template>

<style scoped>
.homepage {
  text-align: center;

  .featured-works {
    text-transform: uppercase;
    font-family: Arial, Helvetica, sans-serif;
  }

}
::v-deep(.page-header .header-image) {
  width: 80%;
  max-width: 100%;
  height: 200px;
  display: block;
}
</style>
