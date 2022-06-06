<template>
  <div id="div-infoxboxer" class="mt-3">
    <div id="div-infoboxer-controls-row" class="row justify-content-center">
      <div
        v-for="item in arrayInfoBoxerItems"
        :key="item.sectionId"
        class="col"
      >
        <b-button
          @click="setSelectedSection(item.sectionId)"
          :pressed="isButtonActive(item.sectionId)"
          class="w-100"
          variant="outline-info"
          >{{ item.sectionName }}</b-button
        >
      </div>
    </div>

    <div class="row mt-4">
      <div class="col">
        <p>{{ arrayInfoBoxerItems[selectedSection].sectionDescription }}</p>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  data() {
    return {
      selectedSection: 0,
    };
  },
  props: {
    arrayInfoBoxerItems: {
      type: Array,
      required: true,
    },
  },
  methods: {
    setSelectedSection(sectionNumber) {
      this.selectedSection = sectionNumber;
    },
    isButtonActive(sectionId) {
      if (sectionId === this.selectedSection) {
        return true;
      } else {
        return false;
      }
    },
  },
  computed: {},
};
</script>