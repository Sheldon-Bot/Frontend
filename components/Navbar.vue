<template>
  <div class="nav">
    <NuxtLink to="/" class="link">Home</NuxtLink>
    <NuxtLink to="/team" class="link">Our Team</NuxtLink>
    <NuxtLink to="/login" class="link">Login</NuxtLink>
  </div>
</template>

<script>
export default {
  name: "Navbar",
}
</script>

<style scoped>
  .nav {
    display: flex;
    justify-content: center;
    padding: 1em;
    gap: 2em;
    width: 100%;
    height: 4em;
    background-color: #35495e;
  }
  .link {
    text-decoration: none;
    color: aliceblue;
    font-size: 1.25em;
  }

  .link:hover {
    color: #559B81;
  }
</style>
