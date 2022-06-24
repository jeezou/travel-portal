<template>
  <div class="card">
    <img :src="img" alt="step card image" class="card__img" />
    <div class="card__description">{{ content }}</div>
  </div>
</template>

<script>
export default {
  name: "StepCard",
  props: {
    img: String,
    content: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 30px;
  width: fit-content;

  &__img {
    width: 100px;
  }

  &__description {
    font-family: "Aleo", serif;
    font-weight: 400;
    font-size: 20px;
    line-height: 24px;
    white-space: none;
    color: #0d606f;
  }
}
</style>
