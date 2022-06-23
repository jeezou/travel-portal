<template>
  <div class="slider">
    <div
      class="slider__slides"
      :style="{ width: sliderWidth, height: height + 'px' }"
    >
      <div class="slider__wrapper" :style="{ left: this.left + 'px' }">
        <template v-for="(slide, index) in slides" :key="slide">
          <Slide
            :img="require('@/assets/' + slide.img + '')"
            :desc="slide.desc"
            :id="index"
            @click="handleSliderRadios(index)"
          />
        </template>
      </div>
    </div>
    <div class="slider__radios">
      <template v-for="(slide, index) in slides" :key="slide">
        <div
          class="slider__radio"
          @click="handleSliderRadios(index)"
          :class="{ 'slider__radio-active': current === index }"
        ></div>
      </template>
    </div>
  </div>
</template>

<script>
import Slide from "@/components/Slide.vue";

export default {
  name: "Slider",
  components: { Slide },
  computed: {
    sliderWidth() {
      return this.slides.length * 800 + "px";
    },
  },
  data() {
    return {
      slides: [
        {
          img: "slide1.jpg",
          desc: "SPAIN",
        },
        {
          img: "slide2.jpg",
          desc: "JAPAN",
        },
        {
          img: "slide3.jpg",
          desc: "USA",
        },
      ],
      current: 1,
      left: 0,
      width: 800,
      height: 800,
    };
  },
  methods: {
    handleSliderRadios(index) {
      this.current = index;
      this.left = -(this.current - 1) * this.width;
    },
  },
};
</script>

<style lang="scss" scoped>
.slider {
  row-gap: 24px;
  display: flex;
  flex-direction: column;

  align-items: center;

  &__slides {
    position: relative;
  }
  &__wrapper {
    width: 100%;
    position: absolute;
    align-items: center;
    display: flex;
    flex-direction: row;

    column-gap: 60px;

    transition: all 0.5s ease-in-out;
  }

  &__radios {
    display: flex;
    column-gap: 10px;
  }

  &__radio {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: rgba(242, 120, 92, 0.5);
    cursor: pointer;

    &-active {
      background: #f2785c;
    }
  }
}
</style>
