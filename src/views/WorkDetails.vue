<script setup>
import { useRoute } from 'vue-router'
import portfolioData from '@/data/portfolio.json'

const route = useRoute()
const id = Number(route.params.id)

const item = portfolioData.find(p => p.id === id)
</script>

<template>
  <div class="details-page" v-if="item">
    <h1>{{ item.title }}</h1>

    <img
      class="main-image"
      :src="`/src/assets/${item.thumbnail}`"
      alt="Main thumbnail image"
    />

    <div class="info">
      <p><strong>Type:</strong> {{ item.type }}</p>
      <p><strong>Medium:</strong> {{ item.medium }}</p>
      <p><strong>Year:</strong> {{ item.dateCreated }}</p>
      <p><strong>Description:</strong> {{ item.description}}</p>
    </div>

    <div class="high-res" v-if="item.highResImages.length">
      <h2>Images</h2>

      <img
        v-for="(img, index) in item.highResImages"
        :key="index"
        :src="img"
        class="extra-image"
      />
    </div>
  </div>

  <p v-else>Item not found.</p>
</template>

<style scoped>
.details-page {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
  color: teal;
}

.main-image {
  width: 300px;
  height: 250px;
  object-fit: cover;
  border: 1px solid black;
  border-radius: 10px;
  margin-bottom: 20px;
}

.info {
  border: 1px solid black;
  border-radius: 15px;
  width: 80%;
  margin: 32px auto 20px auto;
  text-align: center;
  font-size: small;
  font-family: Arial, Helvetica, sans-serif;
  text-transform: uppercase;
  background-color: teal;
  color: white;
}

.extra-image {
  width: 100%;
  margin-top: 16px;
  border-radius: 10px;
  border: 1px solid black;
}
</style>
