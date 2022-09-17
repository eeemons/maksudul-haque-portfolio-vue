<template>
  <div class="items-container" :class="mode === 'dark' ? 'dark' : 'light'">
    <AppNavBar :mode="mode" @toggle="toggle" />
    <PortfolioItem :mode="mode" />
    <AboutItem :mode="mode" />
    <FooterItem :mode="mode" />
  </div>
</template>

<script>
import AppNavBar from "./components/nav-bar-item.vue";
import PortfolioItem from "./components/portfolio-item.vue";
import AboutItem from "./components/about-item.vue";
import FooterItem from "./components/footer-item.vue";

export default {
  name: "App",
  components: { AppNavBar, PortfolioItem, AboutItem, FooterItem },
  data() {
    return {
      mode: "lite",
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
