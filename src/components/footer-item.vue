<script></script>

<template>
  <div class="container">
    <div class="column column-one">
      <div class="social-icons">
        <a href="https://www.facebook.com/eeemons" target="_blank"
          ><img src="../assets/facebook.png" alt=""
        /></a>
        <a href="https://www.instagram.com/eeemons/" target="_blank"
          ><img src="../assets/instagram.png" alt=""
        /></a>
        <a
          href="https://www.linkedin.com/in/maksudul-haque-40984b184/"
          target="_blank"
          ><img src="../assets/linkedin.png" alt=""
        /></a>
        <a href="https://github.com/eeemons" target="_blank"
          ><img src="../assets/github.png" alt=""
        /></a>
      </div>
      <p>Copyright Maksudul Haque</p>
      <p>Designed By Maksudul Haque</p>
    </div>
    <div class="column column-two">
      <p>Contacts</p>
      <p>01684683581</p>
      <p>eeemons@live.com</p>
    </div>
    <div class="column column-three">
      <p>UI/UX Designer</p>
      <p>Front-end Developer</p>
    </div>
  </div>
</template>

<style scoped>
h1,
p,
h2,
h3,
h4 {
  color: #707070;
  font-size: 1.25rem;
}

p:hover {
  color: red;
  cursor: pointer;
}

.container {
  height: 179px;
  background-color: black;
  display: flex;
  justify-content: space-around;
  align-items: center;
  overflow-x: hidden;
}

.social-icons img {
  margin: 3px;
  width: 20px;
  height: 20px;
  cursor: pointer;
  transition: transform 0.5s;
}

.social-icons img:hover {
  transform: scale(1.2);
}

@media screen and (max-width: 426px) {
  h1,
  p,
  h2,
  h3,
  h4 {
    color: #707070;
    font-size: 0.9rem;
  }
  .container {
    flex-direction: column;
    position: relative;
  }
  .column-one {
    position: absolute;
    bottom: 0;
    left: 0;
  }

  .column-two {
    position: absolute;
    top: 0;
    left: 0;
  }

  .column-three {
    position: absolute;
    right: 0;
    bottom: 0;
  }
}

@media screen and (max-width: 320px) {
  h1,
  p,
  h2,
  h3,
  h4 {
    color: #707070;
    font-size: 0.8rem;
  }
}
</style>
