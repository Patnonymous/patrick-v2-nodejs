<template>
  <div id="container-smibuilder" class="container">
    <div id="div-smibuilder-summary-row" class="row">
      <div id="div-smibuilder-summary-col" class="col">
        <h1 id="h1-smibuilder">SmiBuilder</h1>
        <p id="p-smibuilder-summary">Description goes here.</p>
      </div>
    </div>

    <div id="div-smibuilder-infoboxer-row" class="mt-2 row rounded infobox-bg">
      <div id="div-smibuilder-infoboxer-col" class="col">
        <ProjectInfoBoxer :arrayInfoBoxerItems="infoBoxerItems" />
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      infoBoxerItems: [
        {
          sectionId: 0,
          sectionName: "Section 1",
          sectionDescription: "This is section 1.",
        },
        {
          sectionId: 1,
          sectionName: "Section 2",
          sectionDescription: "This is section 2.",
        },
        {
          sectionId: 2,
          sectionName: "Section 3",
          sectionDescription: "This is section 3.",
        },
        {
          sectionId: 3,
          sectionName: "Section 4",
          sectionDescription: "This is section 4.",
        },
      ],
    };
  },
  head: {
    title: "SmiBuilder",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "SmiBuilder project page.",
      },
    ],
  },
};
</script>


<style scoped>
.infobox-bg {
  background-color: rgba(108, 117, 125, 0.1);
}
</style>

