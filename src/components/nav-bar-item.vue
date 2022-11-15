<script>
export default {
  data() {
    return {
      animation: false,
    };
  },
  props: ["mode"],
  methods: {
    toggleAnimation() {
      this.animation = true;
      setTimeout(() => (this.animation = false), 300);
    },
  },
};
</script>

<template>
  <div>
    <nav>
      <section class="top-nav" :class="mode">
        <h1>Maksudul <span>Haque</span></h1>
        <input id="menu-toggle" type="checkbox" />
        <label class="menu-button-container" for="menu-toggle">
          <div class="menu-button"></div>
        </label>

        <ul class="menu">
          <li>Portfolio</li>
          <li>Works</li>
          <li>Contact</li>
          <!-- <li @click="$emit('toggle')" class="mode-switcher">{{ mode }}</li> -->
        </ul>

        <div
          class="square mode-switcher"
          :class="{ squareAnimation: animation }"
          @click="
            $emit('toggle');
            toggleAnimation();
          "
        >
          <div
            class="circle"
            :class="{ circleAnimation: animation }"
            @click="toggleAnimation()"
          >
            {{ mode }}
          </div>
        </div>
      </section>
    </nav>
  </div>
</template>

<style scoped>
h1,
li {
  color: #707070;
  transition: color 1s ease-in-out;
}

h1 span {
  color: rgb(206, 32, 32);
}

.top-nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  height: 50px;
  padding: 1em;
  position: fixed;
  top: 0;
  width: 100%;
  background-color: white;
  z-index: 100;
  transition: background 1s ease-in-out;
}

.menu {
  display: flex;
  flex-direction: row;
  list-style-type: none;
  cursor: pointer;
  margin: 0;
  padding: 0;
}

.menu li:hover {
  color: red;
}

.menu > li {
  margin: 0 1rem;
  overflow: hidden;
}

.menu-button-container {
  display: none;
  height: 100%;
  width: 30px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

#menu-toggle {
  display: none;
}

.menu-button,
.menu-button::before,
.menu-button::after {
  display: block;
  background-color: black;
  position: absolute;
  height: 4px;
  width: 30px;
  transition: transform 400ms cubic-bezier(0.23, 1, 0.32, 1);
  border-radius: 2px;
}

.menu-button::before {
  content: "";
  margin-top: -8px;
}

.menu-button::after {
  content: "";
  margin-top: 8px;
}

#menu-toggle:checked + .menu-button-container .menu-button::before {
  margin-top: 0px;
  transform: rotate(405deg);
}

#menu-toggle:checked + .menu-button-container .menu-button {
  background: rgba(255, 255, 255, 0);
}

#menu-toggle:checked + .menu-button-container .menu-button::after {
  margin-top: 0px;
  transform: rotate(-405deg);
}

.mode-switcher {
  text-transform: capitalize;
}

.dark {
  background: #15202b;
}
.dark h1 {
  color: white;
}
.dark li {
  color: white;
}

.dark .circle {
  color: white;
  border: 1px solid #777;
}

.dark .square {
  color: white;
  border: 1px solid #777;
}

.circle {
  width: 45px;
  height: 45px;
  border-radius: 50%;
  border: 1px solid black;
  position: relative;
  left: 50%;
  top: 50%;
  display: grid;
  place-items: center;
  transform: translate(-50%, -50%);
  cursor: pointer;
  transition: all 0.6s linear;
}

.square {
  width: 75px;
  height: 30px;
  border: 1px solid black;
  cursor: pointer;
  transition: all 0.6s linear;
}

.circle:hover {
  color: red;
}

.circleAnimation {
  transform: translate(-50%, -50%) rotateY(200deg);
}

.squareAnimation {
  transform: rotateZ(360deg) rotateY(200deg);
}

@media (max-width: 700px) {
  .menu-button-container {
    display: flex;
  }
  .menu {
    position: absolute;
    top: 0;
    margin-top: 50px;
    left: 0;
    flex-direction: column;
    width: 100%;
    justify-content: center;
    align-items: center;
  }
  #menu-toggle ~ .menu li {
    height: 0;
    margin: 0;
    padding: 0;
    border: 0;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
  }
  #menu-toggle:checked ~ .menu li {
    border: 1px solid #333;
    height: 2.5em;
    padding: 0.5em;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
  }
  .menu > li {
    display: flex;
    justify-content: center;
    margin: 0;
    padding: 0.5em 0;
    width: 100%;
    color: #707070;
    background-color: #222;
  }
  .menu > li:not(:last-child) {
    border-bottom: 1px solid #444;
  }
}
</style>
