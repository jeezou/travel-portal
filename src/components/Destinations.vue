<template>
  <div class="container">
    <Heading
      :cl="'heading'"
      :level="2"
      :content="'popular destinations'"
      :s="{
        color: '#f2785c',
        fontFamily: 'Red Hat Text',
        fontSize: '40px',
        fontWeight: '500',
        lineHeight: '53px',
        textTransform: 'uppercase',
      }"
    />
    <Slider />
  </div>
</template>

<script>
import Heading from "@/components/Heading.vue";
import Slider from "@/components/Slider.vue";

export default {
  name: "Destinations",
  components: { Heading, Slider },
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
}
</style>
