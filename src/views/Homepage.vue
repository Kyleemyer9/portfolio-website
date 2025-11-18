<script setup>
import portfolioData from '@/data/portfolio.json'
import HeroContainer from '@/components/portfolio/HeroContainer.vue'

const featuredItems = [portfolioData[1], portfolioData[2], portfolioData[3]]
</script>

<template>
  <p>This is my responsive one:</p>
  <hero-container :is-responsive="true" :items="featuredItems" />

  <p>This is my NON-responsive one:</p>
  <hero-container :is-responsive="false" :items="portfolioData" />
</template>

<style scoped>
</style>
