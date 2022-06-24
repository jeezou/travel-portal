<template>
  <div class="container">
    <h1 class="heading">Explore the beauty of the World</h1>
    <p class="par">
      Receive personalized recommendations for countries, hotels, activities and
      more
    </p>
    <div class="introduction">
      <div class="introduction__q">What would you like to do?</div>
      <button type="button" class="introduction__btn">Start Planning</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  components: {},
};
</script>

<style lang="scss" scoped>
* {
  font-family: "Aleo", sans-serif;
  color: #fff;
  font-weight: 700;
}

.container {
  margin-top: 32px;
  display: flex;
  flex-direction: column;
  row-gap: 46px;

  max-width: 892px;

  .heading {
    font-size: 80px;
    line-height: 96px;
  }
}

.par {
  font-size: 20px;
  line-height: 24px;
  font-style: italic;
}

.introduction {
  width: 100%;
  padding: 18px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  border-radius: 16px;

  background: rgba(255, 255, 255, 0.7);

  &__q {
    font-style: italic;
    font-size: 24px;
    font-weight: 400;
    line-height: 29px;
    color: #f2785c;
    margin-left: 23px;
  }

  &__btn {
    font-family: "Red Hat Text", sans-serif;
    font-size: 24px;
    line-height: 32px;
    padding: 13.5px 32.5px;
    border-radius: 10px;
    font-weight: 500;
    background: rgba(13, 96, 111, 1);

    box-shadow: 0px 0px 3px rgba(13, 96, 111, 0.08),
      0px 2px 3px rgba(13, 96, 111, 0.16);
  }
}
</style>
