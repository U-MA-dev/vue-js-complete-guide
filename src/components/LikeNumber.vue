<template>
  <div>
    <p>いいね({{ number / 2 }})</p>
    <button @click="imcrement">+1</button>
  </div>
</template>

<script>
export default {
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
