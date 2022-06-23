<template>
  <main class="main">
    <section class="header">
      <Nav />
      <div class="wrapper">
        <Header />
      </div>
    </section>
    <section class="white">
      <div class="wrapper">
        <Steps />
        <Destinations />
      </div>
    </section>
  </main>
</template>

<script>
import Nav from "@/components/Nav.vue";
import Header from "@/components/Header.vue";
import Steps from "@/components/Steps.vue";
import Destinations from "@/components/Destinations.vue";

export default {
  name: "Main",
  components: { Nav, Header, Steps, Destinations },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.main {
  width: 100vw;
  display: flex;
  flex-direction: column;

  > * {
    display: flex;
    align-items: center;
    flex-direction: column;
    width: 100%;
  }

  .wrapper {
    max-width: 1200px;
    padding: 0 120px;
    width: 100%;
  }

  .header {
    background: url("../assets/header-desktop.png");
    background-size: cover;
    height: 765px;
  }
}
</style>
