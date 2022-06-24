<template>
  <div class="container">
    <h2 class="heading">Popular Destinations</h2>
    <Slider />
    <div class="btn">
      <img src="../assets/bi_arrow-right.svg" alt="arrow" class="btn__arrow" />
      Find More
    </div>
  </div>
</template>

<script>
import Slider from "@/components/Slider.vue";

export default {
  name: "Destinations",
  components: { Slider },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 80px;

  .heading {
    color: #f2785c;
    font-family: "Red Hat Text";
    font-size: 40px;
    font-weight: 500;
    line-height: 53px;
    text-transform: uppercase;
    margin-bottom: 60px;
  }

  .btn {
    margin-top: 40px;
    font-family: "Red Hat Text", sans-serif;
    font-weight: 500;
    display: flex;
    align-items: center;
    column-gap: 10px;
    background: #0d606f;
    color: #fff;
    font-size: 24px;
    line-height: 32px;
    padding: 9.5px 31px;
    border-radius: 10px;
    box-shadow: 0px 0px 3px rgba(13, 96, 111, 0.08),
      0px 2px 3px rgba(13, 96, 111, 0.16);

    cursor: pointer;

    &__arrow {
      width: 40px;
    }
  }
}
</style>
