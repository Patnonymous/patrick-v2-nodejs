<template>
  <div class="container">
    <div class="row">
      <div v-if="!projectName" class="col">
        <h1>Welcome to the projects index. Select a project below!</h1>
        <Carousel />
      </div>

      <div v-else class="col">
        <h1>Projects</h1>
        <h1>{{ projectName }}</h1>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  async asyncData({ params }) {
    const projectName = params.project;
    return { projectName };
  },
  data() {
    return {};
  },
  head: {
    title: "Projects",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Projects I have worked on.",
      },
    ],
  },
};
</script>