<template>
  <nav class="navi">
    <ul class="navigation">
      <li><nuxt-link to="/signup">Sign Up</nuxt-link></li>
      <li><nuxt-link to="/signin">Sign In</nuxt-link></li>
    </ul>
  </nav>
</template>

<style scoped>
  .navi .navigation {
    text-align: center;
  }
  .navi .navigation li {
    display: inline-block;
    margin: 0 10px;
    padding: 0 20px 0 0;
    border-right: 1px solid #0062FF;
  }
  .navi .navigation li:last-child {
    padding: 0;
    border-right: none;
  }
</style>