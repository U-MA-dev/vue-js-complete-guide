<template>
  <div>
    <p>いいね({{ halfNumber }})</p>
    <button @click="imcrement">+1</button>
  </div>
</template>

<script>
export default {
  props: ["totalNumber"],
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
