<template>
  <div class="slider">
    <div
      class="slider__slides"
      :style="{ width: sliderWidth, height: height + 'px' }"
    >
      <div
        class="slider__wrapper"
        :style="{ left: this.left + 'px' }"
        ref="slider-wrapper"
      >
        <template v-for="(slide, index) in $options.slides" :key="slide">
          <Slide
            :img="require(`@/assets/${slide.img}`)"
            :desc="slide.desc"
            :id="index"
            @click="handleSliderRadios(index)"
          />
        </template>
      </div>
    </div>
    <div class="slider__radios">
      <template v-for="(slide, index) in $options.slides" :key="slide">
        <div
          class="slider__radio"
          @click="handleSliderRadios(index)"
          :class="{ 'slider__radio-active': current === index }"
        ></div>
      </template>
    </div>
    <div class="btn">
      <img src="../assets/bi_arrow-right.svg" alt="arrow" class="btn__arrow" />
      Find More
    </div>
  </div>
</template>

<script>
import Slide from "@/components/Slide.vue";

export default {
  name: "Slider",
  components: { Slide },
  slides: [
    {
      img: "slide1.jpg",
      desc: "SPAIN",
    },
    {
      img: "slide3.jpg",
      desc: "USA",
    },
    {
      img: "slide2.jpg",
      desc: "JAPAN",
    },
    {
      img: "slide1.jpg",
      desc: "SPAIN",
    },
    {
      img: "slide3.jpg",
      desc: "USA",
    },
  ],
  computed: {
    sliderWidth() {
      return this.$options.slides.length * 800 + "px";
    },
  },
  data() {
    return {
      current: 0,
      left: 0,
      width: 800,
      height: 800,
    };
  },
  mounted() {
    this.current = Math.floor(this.$options.slides.length / 2);
  },
  methods: {
    handleSliderRadios(index) {
      this.current = index;
      this.left =
        0.5 * (parseInt(this.sliderWidth) - this.width) -
        this.current * this.width;
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
    transition: all 0.3s ease-in-out;

    &:hover {
      background: #f89179;
    }

    &-active {
      background: #f2785c;

      &:hover {
        background: #f2785c;
      }
    }
  }

  .btn {
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
