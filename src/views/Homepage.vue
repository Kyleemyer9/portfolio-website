<script setup>
import portfolioData from '@/data/portfolio.json'
import HeroContainer from '@/components/portfolio/HeroContainer.vue'
import PageHeader from '@/components/PageHeader.vue'

const featuredItems = [
  portfolioData[0],
  portfolioData[1],
  portfolioData[2],
  portfolioData[5],
  portfolioData[4],
]
</script>

<template>
  <div class="homepage">

    <PageHeader
      title="Kylee Myer"
      thumbnail="Banner.jpg"
      icon="Icon0.svg"
    />
<div class="featured-works">
  <h3>Featured Works</h3>
</div>
    <hero-container :is-responsive="true" :items="featuredItems" />
  </div>
</template>

<style scoped>
.homepage {

  .featured-works {
    text-align: center;
    text-transform: uppercase;
    font-family: Arial, Helvetica, sans-serif;
    color: teal;
  }

  .featured-works h3 {
    margin-top: 60px;
    margin-bottom: 16px;
  }

}
::v-deep(.page-header .header-image) {
  width: 100%;
  max-width: 100%;
  height: 200px;
  display: block;
}
</style>
