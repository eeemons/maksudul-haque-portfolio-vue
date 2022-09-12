<template>
  <div>
    <AppNavBar />
    <PortfolioItem />
  </div>
</template>

<script>
import AppNavBar from "./components/nav-bar-item.vue";
import PortfolioItem from "./components/portfolio-item.vue";

export default {
  name: "App",
  components: { AppNavBar, PortfolioItem },
};
</script>

<style></style>
