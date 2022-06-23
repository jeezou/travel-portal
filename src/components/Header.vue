<template>
  <div class="container">
    <Heading
      :cl="'heading'"
      :level="1"
      :content="'Explore the beauty of the World'"
      :s="{
        fontSize: '80px',
        lineHeight: '96px',
      }"
    />
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
import Heading from "@/components/Heading.vue";

export default {
  name: "Header",
  components: { Heading },
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
