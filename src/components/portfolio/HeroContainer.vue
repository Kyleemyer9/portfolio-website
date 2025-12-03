<script setup>
import PortfolioHero from '@/components/portfolio/PortfolioHero.vue'

const props = defineProps({
  items: {
    type: Array,
    required: true,
  },
  isResponsive: {
    type: Boolean,
    required: true,
  },
})
</script>

<template>
  <div
    v-if="props.items.length > 0"
    class="all-items"
    :class="{ 'non-responsive': !props.isResponsive }"
  >
    <PortfolioHero
      v-for="item in props.items"
      :key="item.id"
      :id="item.id"
    :thumbnail="item.thumbnail"
    :title="item.title"
    />
  </div>

  <p v-else>You gotta give me something to work with!</p>
</template>

<style scoped>
div.all-items {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 2rem;
}
</style>

