<template>
  <div>
    <slot name="title" :user="user">
      デフォルトのタイトル
    </slot>
    <slot></slot>
    <!-- <slot name="default"></slot> -->
    <hr />
    <p>いいねの数</p>
    <slot name="number"></slot>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      user: {
        firstName: "Jack",
        lastName: "Donald",
      },
    };
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
