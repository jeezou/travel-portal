<template>
  <h1 v-if="level === 1" :class="cl" :style="s">
    {{ content }}
  </h1>
  <h2 v-if="level === 2" :class="cl" :style="s">
    {{ content }}
  </h2>
</template>

<script>
export default {
  name: "Heading",
  props: {
    cl: String,
    level: Number,
    s: Object,
    content: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

</style>
