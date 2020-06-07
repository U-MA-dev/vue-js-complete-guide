<template>
  <div>
    <LikeHeader>
      <template v-slot:title>
        <h1>こんにちは</h1>
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
