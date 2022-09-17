<script></script>

<template>
  <div class="container">
    <section class="img-container">
      <img src="../assets/myself.jpg" alt="" />
    </section>
    <section class="txt-contaniner">
      <p class="about-txt">&#60; About &#62;</p>
      <p class="vision-txt">
        Welcome to my very own profile, I hope you like the minimalistic design.
        Life should not always be complex. Whatever you think, think simple
        think lazy. Make a new category that is what I call myself lazytistic.
        Yet it will be so soothing and relaxed people around you will have to
        admire the work & get your work through to the person who is watching
        this.
      </p>
      <p class="about-txt">&#60; &#47;About &#62;</p>
    </section>
  </div>
</template>

<style scoped>
p {
  color: #707070;
}

.container {
  display: flex;
  margin: 4rem;
  gap: 5rem;
  align-items: center;
}

.img-container {
  width: 100%;
}

.img-container img {
  width: 100%;
  height: auto;
}

.txt-container {
  flex: 50%;
}
.about-txt {
  font-weight: 800;
}

.vision-txt {
  margin: 2rem;
  text-align: justify;
}

@media screen and (max-width: 426px) {
  .container {
    flex-direction: column;
  }
  .img-container {
    width: 100vw;
  }
  .txt-container {
    width: 100vw;
  }
}
</style>
