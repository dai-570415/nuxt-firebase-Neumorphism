<template>
  <div class="index">
    <div class="nuxt-logo">
      <Logo />
    </div>
    <h2>Welcome! Nuxt.js</h2>
    <AppNavigtion />
  </div>
</template>

<script>
  import AppNavigtion from '~/components/AppNavigation.vue';
  import Logo from '~/components/Logo.vue';

  export default {
    name: 'Index',
    components: { AppNavigtion, Logo },
  }
</script>

<style scoped>
  .index h2 {
    text-align: center;
  }
  ul li {
    display: inline-block;
  }
  .nuxt-logo {
    text-align: center;
    margin: 30px auto 15px;
  }
</style>