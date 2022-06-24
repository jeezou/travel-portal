<template>
  <div class="story">
    <img :src="img" alt="story image" class="story__img" />
    <div class="story__content">
      <h3 class="story__heading">{{ heading }}</h3>
      <p class="story__par">{{ par }}</p>
      <div class="story__read-more">Read More</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Story",
  props: {
    img: String,
    heading: String,
    par: String,
  },
};
</script>

<style lang="scss">
.story {
  width: 100%;

  display: flex;
  column-gap: 40px;

  color: rgba(13, 96, 111, 1);
  font-family: "Aleo", sans-serif;

  &__img {
    width: 400px;
    height: 250px;
    border-radius: 16px;
  }

  &__heading {
    font-size: 35px;
    margin-bottom: 24px;
  }

  &__par {
    font-size: 20px;
    line-height: 24px;
  }

  &__content {
    display: flex;
    flex-direction: column;
  }

  &__read-more {
    text-decoration: underline;
    font-weight: bold;
    font-size: 20px;

    cursor: pointer;
  }
}
</style>
