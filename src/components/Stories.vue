<template>
  <div class="stories">
    <h2 class="heading">Travel Stories</h2>
    <div class="stories__container">
      <div class="wrapper">
        <template v-for="story in $options.stories" :key="story">
          <Story
            :img="require(`@/assets/${story.img}`)"
            :heading="story.heading"
            :par="story.par"
          />
        </template>
      </div>
      <div class="btn">
        <img
          src="../assets/bi_arrow-right.svg"
          alt="arrow"
          class="btn__arrow"
        />
        See More
      </div>
    </div>
  </div>
</template>

<script>
import Story from "@/components/Story.vue";

export default {
  name: "Stories",
  components: { Story },
  stories: [
    {
      img: "story1.png",
      heading: "10 Photos of Attractive Thailand",
      par: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit... ",
    },
    {
      img: "story2.png",
      heading: "Canyonlands National Park, Utah",
      par: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit... ",
    },
    {
      img: "story3.png",
      heading: "I left my heart in the Mountains!",
      par: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit... ",
    },
    {
      img: "story4.png",
      heading: "The Longest journey in my life!",
      par: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Lorem ipsum dolor sit amet, consectetur adipiscing elit... ",
    },
  ],
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.stories {
  display: flex;
  flex-direction: column;
  align-items: center;

  .heading {
    color: #f2785c;
    font-family: "Red Hat Text";
    font-size: 40px;
    font-weight: 500;
    line-height: 53px;
    text-transform: uppercase;

    width: 100vw;
    text-align: center;

    z-index: 1;
    background: #fff;

    padding-bottom: 40px;
  }

  &__container {
    background: rgba(255, 255, 255, 0.7);
    width: 100%;
    padding: 40px 0;

    display: flex;
    flex-direction: column;
    align-items: center;

    .wrapper {
      display: flex;
      flex-direction: column;
      row-gap: 30px;
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
}
</style>
