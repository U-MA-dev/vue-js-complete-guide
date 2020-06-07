<template>
  <div>
    <slot>
      <!-- 何も指定されなかった場合 -->
      デフォルトのタイトル
    </slot>
  </div>
</template>

<script>
export default {
  props: ["headerText"],
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
