<template>
  <div class="signup">
    <h2>Sign up</h2>
    <input type="text" placeholder="Username" v-model="username">
    <input type="password" placeholder="Password" v-model="password">
    <button @click="signUp">会員登録</button>
    <p>
      すでにアカウントをお持ちの方はこちら<br>
      <router-link to="/signin">サインインへ</router-link>
    </p>
  </div>
</template>

<script>
import firebase from 'firebase';

export default {
  name: 'Signup',
  data () {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    signUp: function () {
      firebase.auth().createUserWithEmailAndPassword(this.username, this.password)
        .then(user => {
          alert('Create account: ', user.email);
          this.$router.push('/Sighin');
        })
        .catch(error => {
          alert(error.message);
        })
    }
  }
}
</script>

<style scoped>
  .signup {
    width: 40%;
    margin: 0 auto;
  }
  .signup p {
    font-size: 15px;
    text-align: center;
    line-height: 1.5em;
    margin: 30px 0 0 0;
  }
</style>