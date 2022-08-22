<template>
  <header class="container-fluid bg-dark">
    <nav class="text-white p-4">
      <a href="#" class="text-white me-5">MyWeb</a>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/contact">Contact</router-link>
    </nav>
  </header>
</template>

<script>
export default {
    name: 'MyHeader'
}
</script>

<style lang="scss">
header {

  nav {

    a {
      font-weight: bold;
      color: #fff;

      &.router-link-exact-active {
        color: #42b983;
      }
    }
  }
}
</style>