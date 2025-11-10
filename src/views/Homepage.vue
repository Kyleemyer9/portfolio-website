<script setup>
import portfolioData from '@/data/portfolio.json'
import PortfolioHero from '@/components/portfolio/PortfolioHero.vue'
</script>

<template>
  <div class="all-items">
    <portfolio-hero v-for="thing in portfolioData" :key="thing.id"
      :thumbnail="thing.thumbnail" :title="thing.title"
      />
    </div>
</template>

<style scoped>
div.all-items {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
</style>
