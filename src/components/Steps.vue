<template>
  <div class="container">
    <Heading
      :cl="'heading'"
      :level="2"
      :content="'3 Steps To The Perfect Trip'"
      :s="{
        color: '#f2785c',
        fontFamily: 'Red Hat Text',
        fontSize: '40px',
        fontWeight: '500',
        lineHeight: '53px',
        textTransform: 'uppercase',
      }"
    />
    <div class="cards">
      <template v-for="card in cards" :key="card">
        <StepCard
          :img="require('@/assets/' + card.img + '')"
          :content="card.content"
        />
      </template>
    </div>
  </div>
</template>

<script>
import Heading from "@/components/Heading.vue";
import StepCard from "@/components/StepCard.vue";

export default {
  name: "Steps",
  components: { Heading, StepCard },
  data() {
    return {
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
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.container {
  padding: 80px 0 97px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 40px;

  .cards {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
}
</style>
