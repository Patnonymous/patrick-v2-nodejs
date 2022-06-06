<template>
  <div id="div-infoxboxer" class="mt-3">
    <div id="div-infoboxer-controls-row" class="row justify-content-center">
      <div
        v-for="item in arrayInfoBoxerItems"
        :key="item.sectionId"
        class="col-auto"
      >
        <b-button
          @click="setSelectedSection(item.sectionId)"
          :pressed="isButtonActive(item.sectionId)"
          class="m-auto"
          variant="outline-info"
          >{{ item.sectionName }}</b-button
        >
      </div>
    </div>

    <div class="row mt-4">
      <div class="col">
        <p
          v-if="
            arrayInfoBoxerItems[selectedSection].sectionName != 'Technical Info'
          "
        >
          {{ arrayInfoBoxerItems[selectedSection].sectionDescription }}
        </p>

        <div v-else>
          <div
            class="mb-4"
            v-for="technicalItem in arrayInfoBoxerItems[selectedSection]
              .technical"
            :key="technicalItem.header"
          >
            <h3>{{ technicalItem.header }}</h3>
            <span>{{ technicalItem.description }}</span>
          </div>
        </div>

        <b-carousel
          id="carousel-infoboxer"
          :interval="8000"
          controls
          indicators
          img-width="1920"
          img-height="1030"
          style="text-shadow: 1px 1px 2px #333"
        >
          <b-carousel-slide
            v-for="item in arrayInfoBoxerItems[selectedSection]
              .sectionImageUrls"
            :key="item"
          >
            <template #img>
              <img
                class="d-block img-fluid w-100"
                width="1920"
                height="1030"
                :src="item"
                alt="image slot"
              />
            </template>
          </b-carousel-slide>
        </b-carousel>
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