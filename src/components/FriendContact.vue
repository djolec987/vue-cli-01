<template>
  <li>
    <h2>{{ name }}</h2>
    <button @click="toggleDetails">
      {{ detailsAreVisible ? "Hide" : "Show" }} Details
    </button>
  </li>
  <ul v-if="detailsAreVisible">
    <li><strong>Phone: </strong>{{ phoneNumber }}</li>
    <li><strong>Email: </strong>{{ emailAddress }}</li>
  </ul>
</template>

<script>
export default {
  props: ["name", "phoneNumber", "emailAddress"],
  data() {
    return {
      detailsAreVisible: false,
      friend: {
        id: "sheena",
        name: "Sheena Shaw",
        phone: "3658 998 663",
        email: "shsh@gmail.com",
      },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>
