<template>
  <div>
    <p>いいね({{ number }})</p>
    <button @click="imcrement">+1</button>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      number: 5,
    };
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
