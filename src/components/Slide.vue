<template>
  <div class="slide">
    <div class="slide__description">{{ desc }}</div>
    <img :src="img" :alt="'slider image' + id" class="slide__img" />
  </div>
</template>

<script>
export default {
  name: "Slide",
  props: {
    desc: String,
    img: String,
    id: Number,
  },
  components: {},
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.slide {
  width: 800px;
  height: 800px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;

  border-radius: 16px;

  cursor: pointer;

  &__description {
    z-index: 1;

    position: absolute;
    left: 15px;
    bottom: 40px;

    color: #fff;

    font-size: 32px;
    line-height: 42px;
    font-weight: 500;
    font-family: "Red Hat Text", sans-serif;
  }

  &__img {
    height: 100%;
  }
}
</style>
