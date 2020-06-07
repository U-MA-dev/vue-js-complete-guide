<template>
  <div>
    <LikeHeader>
      <h3>はじめまして</h3>
    </LikeHeader>
    <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
    <button @click="currentComponent = 'Home'">Home</button>
    <button @click="currentComponent = 'About'">About</button>
    <!-- <Home v-if="currentComponent === 'Home'"></Home>
    <About v-else-if="currentComponent === 'About'"></About> -->
    <keep-alive>
      <component :is="currentComponent"></component>
    </keep-alive>
  </div>
</template>

<script>
import LikeHeader from "./components/LikeHeader.vue";
import About from "./components/About.vue";
import Home from "./components/Home.vue";

export default {
  data: function() {
    return {
      number: 10,
      currentComponent: "Home",
    };
  },
  components: {
    LikeHeader: LikeHeader,
    Home: Home,
    About: About,
  },
  methods: {
    incrementNumber: function(event) {
      this.number = event;
    },
  },
};
</script>

<style scoped>
div {
  border: 1px solid blue;
}
</style>
