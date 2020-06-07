<template>
  <div>
    <p>いいね({{ halfNumber }})</p>
    <button @click="imcrement">+1</button>
  </div>
</template>

<script>
export default {
  props: {
    // totalNumber: Number,
    totalNumber: {
      type: Number,
      required: false,
      default: 10,
      // 配列を返す場合にfuncにする
      // default: function() {
      //   return {
      //     number: 5,
      //   };
      // },
    },
  },
  computed: {
    halfNumber() {
      return this.totalNumber / 2;
    },
  },
  methods: {
    imcrement: function() {
      this.number += 1;
    },
  },
};
</script>

<style scoped>
div {
  border: 1px solid red;
}
</style>
