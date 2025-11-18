<script setup>
import NavBar from '@/components/NavBar.vue'
</script>

<template>
  <section class="container">
    <header>
      <nav-bar/>
    </header>

    <section class="content">
      <router-view></router-view>
    </section>

    <footer>Last updated Nov 17, 2025</footer>
  </section>
</template>

<style scoped>
section.container {
  display: flex;
  flex-direction: column;
  gap: 10px;

  > * {
    border: 1px solid white;
  }

  .content {
    background-color: white;
    color: black;
    padding: 10px;
    border-radius: 10px;

    p {
      &:first-of-type {
        margin-top: 0;
      }

      &:last-of-type {
        margin-bottom: 0;
      }
    }
  }

  footer {
    text-align: center;
    padding: 10px;
  }
}
</style>
