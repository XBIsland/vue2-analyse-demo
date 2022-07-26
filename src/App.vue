<template>
  <div id="app">
    <nav>
      app
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
    </nav>
    <div>{{ message }}</div>
    <button @click="handleClick">click</button>
    <HomeView
      @custom="customEvent"
      @click="clickHandler"
      @dblclick.native="dblclickHandler"
    />
    <!-- <router-view /> -->
  </div>
</template>

<script>
import HomeView from "./views/HomeView.vue";
export default {
  components: { HomeView },
  name: "AppVue",
  data() {
    return {
      visiable: false,
      message: "initMessage",
    };
  },
  methods: {
    handleClick() {
      console.log("handleClick", this.$data);
    },
    customEvent() {},
    clickHandler() {},
  },
};
</script>

<style lang="stylus">
#app
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
  margin-top 60px
</style>
