<template>
  <div id="home">
    <h1>{{ msg }}</h1>
    <button @click="googleLogin">Googleアカウントでログイン</button>
  </div>
</template>
<script>
export default {
  name: 'home',
  data() {
    return {
      msg: "Welcome to Mymarkdown"
    };
  },  
  methods: {
    googleLogin: function() {
      firebase.auth().signInWithRedirect(new firebase.auth.GoogleAuthProvider());
    }
  }
};
</script>