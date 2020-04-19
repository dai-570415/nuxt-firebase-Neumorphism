<template>
  <div class="signin">
    <h2>Sign in</h2>
    <input type="text" placeholder="Username" v-model="username">
    <input type="password" placeholder="Password" v-model="password">
    <button @click="signIn">サインイン</button>
    <p>
      アカウントをお持ちでない方はこちら<br>
      <router-link to="/signup">会員登録へ</router-link>
    </p>
  </div>
</template>

<script>
import firebase from 'firebase';

export default {
  name: 'Signin',
  data: function () {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    signIn: function () {
      firebase.auth().signInWithEmailAndPassword(this.username, this.password).then(
        user => {
          alert('Success!');
          this.$router.push('/Hello');
        },
        err => {
          alert(err.message);
        }
      )
    }
  }
}
</script>

<style scoped>
  .signin {
    width: 40%;
    margin: 0 auto;
  }
  .signin p {
    font-size: 15px;
    text-align: center;
    line-height: 1.5em;
    margin: 30px 0 0 0;
  }
</style>