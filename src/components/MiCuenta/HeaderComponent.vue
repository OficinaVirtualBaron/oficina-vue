<template>
  <div class="header-container">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="86"
      height="86"
      fill="currentColor"
      class="bi bi-person-circle"
      viewBox="0 0 16 16"
    >
      <path d="M11 6a3 3 0 1 1-6 0 3 3 0 0 1 6 0z" />
      <path
        fill-rule="evenodd"
        d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm8-7a7 7 0 0 0-5.468 11.37C3.242 11.226 4.805 10 8 10s4.757 1.225 5.468 2.37A7 7 0 0 0 8 1z"
      />
    </svg>
    <h1>{{ name }} {{ lastname }}</h1>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      name: localStorage.getItem("name"),
      lastname: localStorage.getItem("lastname"),
    };
  },
};
</script>

<style scoped>
.header-container {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
}

.header-container h1 {
  margin: 0 10px;
}
</style>
