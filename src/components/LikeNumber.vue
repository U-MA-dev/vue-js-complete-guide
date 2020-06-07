<template>
  <div>
    <p>いいね({{ totalNumber / 2 }})</p>
    <button @click="imcrement">+1</button>
  </div>
</template>

<script>
export default {
  props: ["totalNumber"],
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
