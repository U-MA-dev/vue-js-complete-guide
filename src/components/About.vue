<template>
  <div>
    <p>About</p>
    <input type="text" />
  </div>
</template>

<script>
export default {
  destroyed: function() {
    console.log("destroyed");
  },
};
</script>
