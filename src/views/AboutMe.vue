<script setup>
import PageHeader from '@/components/PageHeader.vue'
import PageInfo from '@/components/PageInfo.vue'
</script>

<template>
  <div class="aboutPage">
    <PageHeader
      title="About Me"
      thumbnail="AboutMe.jpg"
    />

    <PageInfo
      mainText="Hello, my name is Kylee. I am an aspiring graphic designer with an interest
      in digital illustration, visual arts, and UX/web design. I have a passion for creativity
      and I'm always exploring ways to improve my skills as a designer."
      :bullets="[
        '• Graphic Design BFA - University of Minnesota (expected 2026)',
        '• Experienced in Adobe Suite programs (Illustrator, Photoshop, InDesign)',
        '• Experienced in web design programs (Figma, Webstorm)'
      ]"
    />
  </div>
</template>

<style scoped></style>
