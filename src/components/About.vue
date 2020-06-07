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
  deactivated: function() {
    console.log("deactiveted");
  },
  activated: function() {
    console.log("activeted");
  },
};
</script>
