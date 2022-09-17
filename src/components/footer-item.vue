<script></script>

<template>
  <div class="container">
    <div class="column column-one">
      <p>Socials</p>
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

@media screen and (max-width: 425px) {
  h1,
  p,
  h2,
  h3,
  h4 {
    color: #707070;
    font-size: 1rem;
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
</style>
