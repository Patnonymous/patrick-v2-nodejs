<template>
  <div>
    <b-carousel
      id="carousel-projects"
      :interval="12000"
      controls
      indicators
      img-width="1920"
      img-height="1030"
      style="text-shadow: 1px 1px 2px #333"
    >
      <!-- Loops through the slides data. -->
      <div v-for="item in slidesDataArray" :key="item.slideId">
        <!-- Surrounding the b-carousel-slide with a link allows for easy linking to project pages. -->
        <b-link :to="item.projectUrl">
          <b-carousel-slide :caption="item.slideCaption" :text="item.slideText">
            <template #img>
              <img
                class="d-block img-fluid w-100 rounded"
                :class="{ 'low-brightness': item.lowerBrightness }"
                width="1920"
                height="1030"
                :src="item.slideImgUrl"
                :alt="item.slideAltText"
              />
            </template>
          </b-carousel-slide>
        </b-link>
      </div>
    </b-carousel>
  </div>
</template>

<script>
// Import the slide images for use in the v-for looped carousel.
import smiBuilderImage from "~/assets/smibuilder/1viewing.png";
import wifiWizardImage from "~/assets/wifiwizard/1mainmenu.png";

/**
 * @description Carousel to display projects.
 *
 * This is bad cause it's not a true component, data is harcoded. Should be changed to use
 * props and dynamic data.
 */
export default {
  data() {
    return {
      /**
       * @description Array holds data for each slide item.
       * @param {Number} slideId - Slide data ID
       * @param {String} slideCaption - The main larger text to display for the slide.
       * @param {String} slideText - Smaller descriptive text under the Caption.
       * @param {String} slideImgUrl - Url path to the display image.
       * @param {String} slideAltText - Alternate text if the image fails to load.
       * @param {Boolean} lowerBrightness - Controls if the slides image should be darker to accommodate the control scheme.
       */
      slidesDataArray: [
        {
          slideId: 1,
          slideCaption: "SmiBuilder",
          slideText: "Character build planner and publisher for a game.",
          slideImgUrl: smiBuilderImage,
          slideAltText: "Main page for SmiBuilder.",
          lowerBrightness: true,
          projectUrl: "/projects/SmiBuilder",
        },
        {
          slideId: 2,
          slideCaption: "WifiWizard",
          slideText: "WEBGL Educational Game for Mohawk College.",
          slideImgUrl: wifiWizardImage,
          slideAltText: "The help page for WifiWizard.",
          lowerBrightness: false,
          projectUrl: "/projects/WifiWizard",
        },
      ],
    };
  },
  methods: {},
};
</script>


<style scoped>
.low-brightness {
  filter: brightness(50%);
}
</style>