<template>
  <div class="container">
    <header>
      <nuxt-link to="/">Neomo Design</nuxt-link>
    </header>
    <main class="main">
      <nuxt />
    </main>
    <footer class="footer">
        ©︎2020 Nuxt
    </footer>
  </div>
</template>

<script>
  export default {
    
  }
</script>
  
<style>
  *,
  *:before,
  *:after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    background: #EBECF0;
  }
  html {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
      Roboto, 'Helvetica Neue', Arial, sans-serif;
    font-size: 16px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
  }
  a {
    color: #0062FF;
    text-decoration: none;
  }
  ul li {
    list-style: none;
  }
  .container {
    width: 95%;
    margin: 20px auto;
  }
  .main {
    width: 100%;
    margin: 50px auto;
  }
  .main h2 {
    font-size: 40px;
    font-weight: 100;
    text-align: left;
    color: rgb(78, 78, 78);
    margin: 0 0 25px 0;
    text-shadow: 2px 2px 0 #fff;
  }
  /* ログインフォーム */
  button,
  input {
    border: 0;
    outline: 0;
    font-size: 15px;
    border-radius: 320px;
    padding: 15px;
    background-color: #EBECF0;
    text-shadow: 1px 1px 0 #FFF;
  }
  label {
    display: block;
    margin-bottom: 25px;
    width: 100%;
  }
  input {
    box-shadow: 2px 2px 5px #BABECC inset, -5px -5px 10px #FFF inset;
    width: 100%;
    margin: 0 0 20px 0;
    transition: .5s;
  }
  input:focus {
    box-shadow: 1px 1px 2px #BABECC inset, -1px -1px 2px #FFF inset;
  }
  button {
    font-size: 15px;
    font-weight: 300;
    color: #0062FF;
    box-shadow: -5px -5px 20px #FFF, 5px 5px 20px #BABECC;
    transition: .5s;
    cursor: pointer;
    width: 100%;
    margin: 0 0 15px 0;
  }
  button:hover {
    box-shadow: -2px -2px 5px #FFF, 2px 2px 5px #BABECC;
  }
  button:active {
    box-shadow: inset 1px 1px 2px #BABECC, inset -1px -1px 2px #FFF;
  }
  footer {
    font-size: 12px;
    font-weight: 100;
    text-align: center;
    position: fixed;
    bottom: 5%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
</style>
