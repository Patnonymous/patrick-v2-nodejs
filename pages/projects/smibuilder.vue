<template>
  <div id="container-smibuilder" class="container">
    <div id="div-smibuilder-summary-row" class="row">
      <div id="div-smibuilder-summary-col" class="col">
        <h1 id="h1-smibuilder">SmiBuilder</h1>
        <p id="p-smibuilder-summary">
          Character build planner for a game. Users can log in, create a
          character planner then publish it. Members can rate and favourite
          builds, as well as make comments on them. Admins can view site stats
          including user activity, most popular characters and the most popular
          items.
        </p>
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
// SmiBuilderImages
import smiBuilderViewing from "~/assets/smibuilder/1viewing.png";
import smiBuilderAnonymous from "~/assets/smibuilder/2anonymousbuildview.png";
import smiBuilderMemberGodsFiltering from "~/assets/smibuilder/3membergodsfiltering.png";
import smiBuilderMemberItemFilters from "~/assets/smibuilder/4memberitemfilters.png";
import smiBuilderMemberPublishing from "~/assets/smibuilder/5memberpublishing.png";
import smiBuilderBuildNameFilter from "~/assets/smibuilder/6memberbuildnamefilter.png";
import smiBuilderMemberBuildComment from "~/assets/smibuilder/7memberbuildcomment.png";
import smiBuilderMemberFavourites from "~/assets/smibuilder/8memberfavourites.png";
import smiBuilderMemberUserAccount from "~/assets/smibuilder/9memberuseraccount.png";
import smiBuilderAdminStats from "~/assets/smibuilder/10adminstats.png";

export default {
  data() {
    return {
      infoBoxerItems: [
        {
          sectionId: 0,
          sectionName: "Info Front and Center",
          sectionDescription:
            "No messing with menus and submenus. SmiBuilder build data and controls follow a natural flow.",
          sectionImageUrls: [smiBuilderViewing, smiBuilderAnonymous],
        },
        {
          sectionId: 1,
          sectionName: "Publishing",
          sectionDescription:
            "SmiBuilder allows users to publish their builds, rate builds and leave comements.",
          sectionImageUrls: [
            smiBuilderMemberPublishing,
            smiBuilderMemberBuildComment,
          ],
        },
        {
          sectionId: 2,
          sectionName: "Robust Filtering",
          sectionDescription:
            "Users can filter all aspects of the site to find the characters, items, and builds they are looking for.",
          sectionImageUrls: [
            smiBuilderMemberGodsFiltering,
            smiBuilderMemberItemFilters,
            smiBuilderBuildNameFilter,
          ],
        },
        {
          sectionId: 3,
          sectionName: "Favourites",
          sectionDescription:
            "No messing with bookmarks or links, SmiBuilder supports favouriting.",
          sectionImageUrls: [smiBuilderMemberFavourites],
        },
        {
          sectionId: 4,
          sectionName: "Multiple Account Types",
          sectionDescription:
            "Authorization is controlled using multiple account types. Supports anonymous, members and admins. Users can change their passwords, and purge their accounts.",
          sectionImageUrls: [smiBuilderMemberUserAccount, smiBuilderAdminStats],
        },
        {
          sectionId: 5,
          sectionName: "Technical Info",
          sectionDescription: "",
          sectionImageUrls: [],
          technical: [
            { header: "Team", description: "Solo project." },
            {
              header: "Project Components",
              description:
                "A frontend communicates to the backend API. The API handles database queries and data processing.",
            },
            {
              header: "Code Tracking",
              description:
                "Repos on Github. Branched and pushed when parts were finished.",
            },
            {
              header: "Language, Tech, Tech Stack",
              description:
                "NodeJS, Vue using Nuxt for front facing client. ExpressJS for backend. Styled using Bootstrap and Bootstrap Vue.",
            },
            {
              header: "Account and Persistent Data",
              description:
                "Accounts and persistent data used. Saved to an SQL database.",
            },
            {
              header: "Hosting",
              description:
                "The client, API and database were deployed and hosted on Microsoft Azure.",
            },
            {
              header: "Other Components",
              description:
                "This site was designed and planned using Figma, an online collaborative interface design tool.",
            },
          ],
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

