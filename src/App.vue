<script setup></script>

<template>
 <section class="container">
   <header>My header here</header>

   <section>
     <router-view></router-view>
   </section>

   <footer>Footer here</footer>
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
  }
}
</style>
