<template>
  <div id="container-wifiwizard" class="container">
    <div id="div-wifiwizard-summary-row" class="row">
      <div id="div-wifiwizard-summary-col" class="col">
        <h1 id="h1-wifiwizard">WifiWizard</h1>
        <p id="p-wifiwizard-summary">
          WifiWizard is an educational game created using Unity. We were
          contracted by one of the networking professors at Mohawk to create a
          prototype educational game that allows students to place network
          access point antennas, and see the area that they affect. The goal of
          the game is to cover as much area as possible using a limited amount
          of router antennas and access points.
        </p>
        <a href="https://github.com/Patnonymous/WifiWizard">Application Repo</a>
      </div>
    </div>

    <div id="div-wifiwizard-infoboxer-row" class="mt-2 row rounded infobox-bg">
      <div id="div-wifiwizard-infoboxer-col" class="col">
        <ProjectInfoBoxer :arrayInfoBoxerItems="infoBoxerItems" />
      </div>
    </div>
  </div>
</template>


<script>
// WifiWizard images.
import wifiWizardMainMenu from "~/assets/wifiwizard/1mainmenu.png";
import wifiWizardGameImage1 from "~/assets/wifiwizard/2gameimage1.png";
import wifiWizardGameImage2 from "~/assets/wifiwizard/3gameimage2.png";
import wifiWizardPauseMenu from "~/assets/wifiwizard/4pausemenu.png";

export default {
  data() {
    return {
      infoBoxerItems: [
        {
          sectionId: 0,
          sectionName: "Hosted Using WEBGL",
          sectionDescription:
            "By leveraging powerful WEBGL tech, the game can be hosted and played on a web page.",
          sectionImageUrls: [wifiWizardMainMenu],
        },
        {
          sectionId: 1,
          sectionName: "Inventory Full of Antennas",
          sectionDescription:
            "The player must cover relevant areas using their limited supply of antennas and access points.",
          sectionImageUrls: [wifiWizardGameImage1, wifiWizardGameImage2],
        },
        {
          sectionId: 2,
          sectionName: "Score Exporting",
          sectionDescription:
            "The player can export their score to a file, they can then send that score to their instructor for processing.",
          sectionImageUrls: [wifiWizardPauseMenu],
        },
        {
          sectionId: 3,
          sectionName: "Technical Info",
          sectionDescription: "",
          sectionImageUrls: [],
          technical: [
            { header: "Team", description: "This was a team project." },
            {
              header: "Project Components",
              description:
                "A Unity game, and a Python script provided to instructors for score processing.",
            },
            {
              header: "Code Tracking",
              description:
                "Repos on Github. Branched and pushed when parts were finished. Basic tests were done to check for major bugs.",
            },
            {
              header: "Language, Tech, Tech Stack",
              description:
                "Unity C# for the game component. Python for the instructors score processing script.",
            },
            {
              header: "Account and Persistent Data",
              description:
                "Not required or in the scope of this project. Scores can be exported to a file though.",
            },
            {
              header: "Hosting",
              description:
                "The game could be run locally or hosted using WEBGL.",
            },
            {
              header: "Other Components",
              description:
                "The project was done according to provided specifications and input from a networking professor at Mohawk.",
            },
          ],
        },
      ],
    };
  },
  head: {
    title: "WifiWizard",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "WifiWizard project page.",
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

