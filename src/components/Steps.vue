<template>
  <div class="container">
    <h2 class="heading">3 Steps To The Perfect Trip</h2>
    <div class="cards">
      <template v-for="card in $options.cards" :key="card">
        <StepCard
          :img="require(`@/assets/${card.img}`)"
          :content="card.content"
        />
      </template>
    </div>
  </div>
</template>

<script>
import StepCard from "@/components/StepCard.vue";

export default {
  name: "Steps",
  components: { StepCard },
  cards: [
    {
      img: "step1.svg",
      content: "Tell us what you want to do",
    },
    {
      img: "step2.svg",
      content: "Share us preferable dates ",
    },
    {
      img: "step3.svg",
      content: "We will give you recommendations",
    },
  ],
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.container {
  padding: 80px 0 97px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 40px;

  .heading {
    color: #f2785c;
    font-family: "Red Hat Text";
    font-size: 40px;
    font-weight: 500;
    line-height: 53px;
    text-transform: uppercase;
  }

  .cards {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
}
</style>
