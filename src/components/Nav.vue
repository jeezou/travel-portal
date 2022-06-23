<template>
  <nav class="nav-bar">
    <div class="container">
      <div class="logo">
        <img src="../assets/logo.svg" alt="logo" class="logo__img" />
        <span class="logo__content">Travel Portal</span>
      </div>
      <div class="links">
        <a class="hiw"> How It Works </a>
        <a class="pyt"> Plan Your Trip </a>
        <a class="dest"> Destination </a>
        <a class="travel"> Travel Stories </a>
      </div>
      <button type="button" class="login">Login</button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.nav-bar {
  width: 100%;
  display: flex;
  justify-content: center;
  background: rgba(242, 120, 92, 0.7);
  box-shadow: 0px 4px 4px rgba(13, 96, 111, 0.5);
  font-family: "Red Hat Text";
  font-weight: 500;
  font-size: 16px;
  padding: 25px 0;
  color: #ffffff;

  .container {
    max-width: 1200px;
    width: 100%;
    padding: 0 120px;

    display: flex;
    justify-content: space-between;
  }

  .logo {
    font-family: "Magra", sans-serif;
    font-size: 32px;
    font-weight: 600;

    display: flex;
    column-gap: 6px;
    height: fit-content;

    &__img {
      height: 30px;
      width: 30px;
    }

    &__content {
      align-self: flex-end;
    }
  }

  .links {
    display: flex;
    column-gap: 42px;
    align-self: center;
  }

  .login {
    padding: 10px 30px;
    background: #0d606f;
    color: #ffffff;
    border-radius: 10px;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25),
      0px 2px 3px rgba(13, 96, 111, 0.16);
  }
}
</style>
