<template>
  <div v-show="!showMain" class="preloader">
    <Preloader />
  </div>
  <div
    v-show="showMain"
    class="items-container"
    :class="mode === 'dark' ? 'dark' : 'light'"
  >
    <AppNavBar :mode="mode" @toggle="toggle" />
    <PortfolioItem :mode="mode" />
    <AboutItem :mode="mode" />
    <FooterItem />
  </div>
</template>

<script>
import Preloader from "./components/preloader-item.vue";
import AppNavBar from "./components/nav-bar-item.vue";
import PortfolioItem from "./components/portfolio-item.vue";
import AboutItem from "./components/about-item.vue";
import FooterItem from "./components/footer-item.vue";

export default {
  name: "App",
  components: { AppNavBar, PortfolioItem, AboutItem, FooterItem, Preloader },
  data() {
    return {
      mode: "lite",
      showMain: false,
    };
  },
  methods: {
    toggle() {
      if (this.mode === "dark") {
        this.mode = "lite";
      } else {
        this.mode = "dark";
      }
    },
  },
  created() {
    setTimeout(() => (this.showMain = true), 4000);
  },
};
</script>

<style>
.items-container {
  background: white;
  transition: background 1s ease-in-out;
}
.dark {
  background: #0a1015;
}
</style>
