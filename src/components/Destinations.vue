<template>
  <div class="container">
    <h2 class="heading">popular destinations</h2>
    <Slider />
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

  row-gap: 60px;

  margin-bottom: 40px;

  .heading {
    color: #f2785c;
    font-family: "Red Hat Text";
    font-size: 40px;
    font-weight: 500;
    line-height: 53px;
    text-transform: uppercase;
  }
}
</style>
