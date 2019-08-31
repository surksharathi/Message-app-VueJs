<template>
  <div id="app">
    <h1>My Messaging App!</h1>
    <MessageList />
  </div>
</template>

<script>
import MessageList from "./components/MessageList.vue";

export default {
  components: {
    MessageList
  }
};
</script>

<style>
body {
  background-image: linear-gradient(120deg, #f6d365 0%, #fda085 100%);
  height: 100vh;
}

#app {
  max-width: 400px;
  margin: 0 auto;
  padding-top: 200px;
  line-height: 1.4;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #32485f;
}

h1 {
  text-align: center;
}
@media (max-width: 450px) {
  body {
    text-align: center;
    margin-left: 50px;
    margin-right: 50px;
    margin-top: 50px;
    height: 200px;
  }
}
</style>