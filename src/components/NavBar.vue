<script setup>
</script>

<template>
  <div class="container">
    <div class="links">
      <p class="links-title">Kylee Myer</p>
      <router-link :to="{name: 'home'}">Home</router-link>

      <router-link :to="{name: 'about-me'}">About Me</router-link>

      <router-link :to="{name: 'my-work'}">My Work</router-link>

      <router-link :to="{name: 'contact-me'}">Contact Me</router-link>
    </div>
  </div>
</template>

<style scoped>

div.container {
  width: 100%;
  display: flex;
  justify-content: center;
}

div.links {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: flex-start;
}

.links-title {
  color: white;
  font-weight: bold;
  margin-left: 20px;
}

div.links a {
  color: white;
  text-decoration: none;
  padding: 5px;
}

div.links a:hover {
  background-color: white;
  color: teal;
}

@media (width > 600px) {
  div.links {
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;
  }

  .links-title {
    margin-right: auto;
    margin-left: 20px;
  }
}


</style>
