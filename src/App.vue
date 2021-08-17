<template>
  <div id="app">
    <button id="toggle" @click="activate">Click Here</button>
    <TweetCon></TweetCon> 
  </div>
</template>

<script>
import TweetCon from './components/tweetCon.vue'

export default {
  name: 'App',
  components: {
    TweetCon,
    },

    methods : {
      activate: function() {
      console.log("button clicked");
      this.$root.$emit('isActive');
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: lightblue;
}
</style>
