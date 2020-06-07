<template>
  <div>
    <LikeHeader>
      <h1>トータルのいいね数</h1>
      <h2>{{ number }}</h2>
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
