<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1>About</h1>
        <p>
          <a href="#" @click="toggleImage">Hello There!</a> Welcome to my
          portfolio site. Here you'll find projects, relevant links, my resume
          and contact information. If you're looking for projects, you're gonna
          want to <b-link to="/projects">go here.</b-link> Need to contact me?
          <b-link to="/contact">look here.</b-link>
        </p>
      </div>
    </div>

    <div class="row justify-content-center">
      <div class="col-auto">
        <Transition name="fade">
          <b-img
            v-if="showImage"
            :src="helloUrl"
            fluid
            alt="Hello there gif"
          ></b-img>
        </Transition>
      </div>
    </div>
  </div>
</template>


<script>
// Imports.
import helloThere from "~/assets/about/hello-there.webp";
export default {
  data() {
    return {
      helloUrl: helloThere,
      showImage: false,
    };
  },
  methods: {
    toggleImage() {
      console.log("Showing image.");
      this.showImage = !this.showImage;
    },
  },
  head: {
    title: "About",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "About me.",
      },
    ],
  },
};
</script>

<style scoped>
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s ease;
}

.fade-enter-to {
  opacity: 1;
}

.fade-enter {
  opacity: 0;
}
</style>