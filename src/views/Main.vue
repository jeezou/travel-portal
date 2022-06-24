<template>
  <main class="main">
    <section class="header">
      <Nav />
      <div class="wrapper">
        <Header />
      </div>
    </section>
    <section class="light">
      <div class="wrapper">
        <Steps />
        <Destinations />
      </div>
    </section>
    <section class="img-bg">
      <Stories />
      <footer class="footer">
        <div class="wrapper">
          <a class="footer__gh" href="https://github.com/jeezou">
            <img class="icon" src="../assets/gh.png" alt="gh icon" />
          </a>
          <div class="footer__rights">All Rights Reserved © Travel Portal</div>
          <div class="footer__socials">
            <a class="footer__social" href="#">
              <img src="../assets/inst.svg" alt="social icon" />
            </a>
            <a class="footer__social" href="#">
              <img src="../assets/yt.svg" alt="social icon" />
            </a>
            <a class="footer__social" href="#">
              <img src="../assets/twitter.svg" alt="social icon" />
            </a>
          </div>
        </div>
      </footer>
    </section>
  </main>
</template>

<script>
import Nav from "@/components/Nav.vue";
import Header from "@/components/Header.vue";
import Steps from "@/components/Steps.vue";
import Destinations from "@/components/Destinations.vue";
import Stories from "@/components/Stories.vue";

export default {
  name: "Main",
  components: { Nav, Header, Steps, Destinations, Stories },
};
</script>

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

  .img-bg {
    background: url("../assets/footer-bg.png");
    background-size: cover;

    .footer {
      display: flex;
      width: 100%;
      justify-content: center;
      .wrapper {
        font-family: "Red Hat Text", sans-serif;
        font-size: 16px;
        line-height: 21px;
        font-weight: 500;
        color: #fff;
        padding: 13px 0;

        display: flex;
        width: 100%;

        justify-content: space-between;

        position: relative;

        .footer__gh {
          cursor: pointer;
          background: #fff;
          border-radius: 50%;
          .icon {
            width: 34px;
          }
        }

        .footer__rights {
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }

        .footer__socials {
          cursor: pointer;
          display: flex;
          column-gap: 20px;
        }
      }
    }
  }
}
</style>
