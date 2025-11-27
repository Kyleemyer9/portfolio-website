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
      mainText="I can be contacted through these methods:"
      :bullets="[
    '• Email: kyleemyer9@gmail.com',
    '• Phone Number: (612) 300-2780',
    `• LinkedIn: <a href='https://www.linkedin.com/in/kylee-myer/' target='_blank'>Kylee Myer</a>`
  ]"
    />
  </div>
</template>

<style scoped></style>
