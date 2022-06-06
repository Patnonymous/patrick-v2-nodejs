<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1>Welcome to the projects index. Select a project below!</h1>
        <Carousel />
      </div>
    </div>
  </div>
</template>


<script>
export default {
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