<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1>Contact info.</h1>
        <p>See resume and LinkedIn for phone number and email.</p>

        <p>
          <b-link
            href="https://www.linkedin.com/in/patrick-williamson-b88b33201/"
            >LinkedIn</b-link
          >
        </p>
        <p>
          <b-link href="https://github.com/Patnonymous">Github</b-link>
        </p>
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
    title: "Contact",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "My contact information.",
      },
    ],
  },
};
</script>