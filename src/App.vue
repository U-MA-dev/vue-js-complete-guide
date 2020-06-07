<template>
  <div>
    <LikeHeader>
      <template v-slot:title>
        <h2>こんにちは</h2>
      </template>
      <template v-slot:default>
        <h2>みなさん</h2>
        <h3>はじめまして</h3>
        <p>よろしくお願いします</p>
      </template>
      <template v-slot:number>
        <p>{{ number }}</p>
      </template>
    </LikeHeader>
    <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
    <LikeNumber :total-number="number"></LikeNumber>
  </div>
</template>

<script>
import LikeHeader from "./components/LikeHeader.vue";

export default {
  data: function() {
    return {
      number: 10,
    };
  },
  components: {
    LikeHeader: LikeHeader,
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
