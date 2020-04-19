<template>
  <div class="hello">
    <h2>Hello!!<span>{{ email }}</span></h2>
    <a @click="signOut">Sign out</a>
  </div>
</template>

<script>
import firebase from 'firebase';

export default {
  name: 'Hello',
  data () {
    return {
      email: firebase.auth().currentUser.email,
    }
  },
  methods: {
    signOut: function () {
      firebase.auth().signOut().then(() => {
        this.$router.push('/Signin');
      })
    }
  }
}
</script>

<style scoped>
  .hello,
  .hello h2 {
    text-align: center;
  }
  .hello h2 span {
    display: block;
    font-size: 16px;
  }
</style>