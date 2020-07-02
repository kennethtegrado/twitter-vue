<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Header tabTitle="Home"/>

    <TweetBlock />

    <div v-bind:key="tweet.id" v-for="tweet in tweets">
      <PostBlock v-bind:tweet="tweet"/>
    </div>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import TweetBlock from './components/TweetBlock.vue'
import PostBlock from './components/PostBlock.vue'

export default {
  name: 'App',
  components: {
    Header,
    PostBlock,
    TweetBlock
  },
  data() {
    return {
      tweets: [{
        id: 1,
        user_img: "xi.jpg",
        username: "Si num pong",
        usertag: "@xijohnpong",
        time_elapsed: "18h",
        content: "Your islands are mine madafakas!!!!Your islands are mine madafakas!!!!Your islands are mine madafakas!!!!Your islands are mine madafakas!!!!",
        content_img: "vicopost.jpg"
      }],
      user: {
        name: "Kuleng",
        username: "khalsuu",
        user_photo: "me3.jpeg"
      }
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

  border: 1px solid black;
  margin-left: auto;
  margin-right: auto;
}

@media only screen and (min-width: 576px) {

  #app {
  width: 50vw;
  left: 25%;
  }
}
</style>
