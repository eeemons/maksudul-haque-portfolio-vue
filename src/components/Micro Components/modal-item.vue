<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleIsOpen() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>

<template>
  <div class="container">
    <button @click="toggleIsOpen()">Details</button>
    <teleport to="body">
      <div class="modal" v-if="isOpen">
        <div class="modal-main-content">
          <section class="Project-details">
            <img class="project-img" src="../../assets/demo.jpg" alt="" />
            <h1>Project Details</h1>
            <h2>Name: Project_title</h2>
            <h3>Technologies used: <span>Technologies</span></h3>
            <span class="bold-title"
              >Project inspirations:
              <span class="normal-txt"
                >Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                Laudantium saepe velit harum alias quam voluptates fugiat
                accusantium maiores officiis odit! Corporis quae impedit earum
                placeat alias, id dolores porro! Assumenda?</span
              ></span
            >
          </section>
          <button @click="toggleIsOpen()">Close</button>
        </div>
      </div>
    </teleport>
  </div>
</template>

<style scoped>
.container {
  position: relative;
}

.modal {
  position: absolute;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.1);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal > div {
  background-color: #fff;
  padding: 50px;
  border-radius: 10px;
  max-width: 800px;
}

button {
  border: 1px solid black;
  padding: 8px;
  margin-bottom: 10px;
  outline: none;
  color: #707070;
  text-align: center;
  text-decoration: none;
  background-color: transparent;
  font-family: inherit;
  cursor: pointer;
}

.project-img {
  width: 100%;
  aspect-ratio: 16/9;
  max-width: 400px;
}

.modal-main-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.Project-details {
  margin-top: 5em;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.Project-details > * {
  margin: 10px;
}

.bold-title {
  font-weight: bold;
  text-align: justify;
}

.normal-txt {
  font-weight: normal;
  text-align: justify;
}
</style>
