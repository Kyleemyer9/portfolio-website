<script setup>
import PageHeader from '@/components/PageHeader.vue'
import PageInfo from '@/components/PageInfo.vue'
</script>

<template>
  <div class="contactPage">
    <PageHeader
      title="Contact Me"
      thumbnail="ContactMe.jpg"
    />

    <PageInfo
      mainText="Content here"
      :bullets="[
        'Bullet 1',
        'Bullet 2',
        'Bullet 3'
      ]"
    />
  </div>
</template>

<style scoped></style>
