<script>
import WorkCard from "./Micro Components/work-card.vue";
import TypeWriter from "./Micro Components/type-writer.vue";
export default {
  components: { WorkCard, TypeWriter },
};
</script>
<template>
  <div>
    <section class="message-section">
      <TypeWriter />
      <p>Creating Your dream and then making your dream come to life</p>
      <p>A front-end web developer with a hobby of designing UI/UX</p>
    </section>

    <section class="skill-section">
      <p>Skills</p>
      <div class="skill-imgs">
        <img src="../assets/html.png" alt="" />
        <img src="../assets/css.webp" alt="" />
        <img src="../assets/vue.webp" alt="" />
        <img src="../assets/react.png" alt="" />
        <img src="../assets/figma.png" alt="" />
        <img src="../assets/xd.png" alt="" />
      </div>
    </section>
    <div class="work-section">
      <p class="work-title">Work</p>
      <section class="work-card-section">
        <WorkCard />
        <WorkCard />
        <WorkCard />
        <WorkCard />
        <WorkCard />
      </section>
    </div>
  </div>
</template>

<style scoped>
h1 {
  color: #707070;
  font-size: 3.125rem;
  text-align: center;
}
p {
  color: #707070;
  font-weight: 900;
  font-size: 1.25rem;
  text-align: center;
}

.message-section {
  margin: 3rem;
}
.skill-section {
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: center;
  margin: 6rem 4rem;
  gap: 5rem;
}

.skill-section img {
  width: 80px;
  height: 80px;
}

.work-card-section {
  display: flex;
  justify-content: space-around;
}

.work-title {
  margin: 10px;
  position: relative;
}

@media screen and (max-width: 426px) {
  .skill-section {
    margin: 4rem 0;
  }
  .work-section {
    width: 100%;
  }
  .work-card-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
  }
  .skill-section img {
    width: 40px;
    height: 40px;
  }
}
@media screen and (max-width: 350px) {
  .skill-section {
    margin: 4rem 0;
  }

  .skill-section img {
    width: 50px;
    height: 50px;
  }
}
</style>
