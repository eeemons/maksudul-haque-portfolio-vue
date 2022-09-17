<template>
  <div class="items-container">
    <AppNavBar />
    <PortfolioItem />
    <AboutItem />
    <FooterItem />
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
};
</script>

<style></style>
