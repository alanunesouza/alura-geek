<script setup>
import SearchBarDesktop from "./SearchBarDesktop.vue";
</script>

<template>
  <div class="header container">
    <div class="content">
      <div class="left-content">
        <v-img height="28" width="100" max-width="100" :src="logo"></v-img>
      </div>

      <div class="only-desktop">
        <SearchBarDesktop />
      </div>

      <div class="right-content">
        <v-btn width="133" elevation="2" outlined color="primary">Login</v-btn>
      </div>

      <button class="button-search-mobile" @click="toggleOpenSearchBarMobile()">
        <svg
          aria-hidden="true"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
          ></path>
        </svg>
      </button>
    </div>

    <div class="searchbar-mobile" v-show="openSearchBarMobile">
      <SearchBarDesktop />
    </div>
  </div>
</template>

<style scoped>
.header.container {
  max-width: 1366px;
  background-color: #ffffff;
  top: 0;
  padding: 18px 16px;
  border-bottom: 1px solid;
  display: flex;
  flex-direction: column;
}

.header .content {
  display: flex;
  flex: 1;
  justify-content: space-evenly;
  align-items: center;
  gap: 8px;
}

.header .left-content {
  display: flex;
  align-items: center;
  gap: 18px;
}

.header .right-content {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.header .button-search-mobile {
  display: flex;
  padding: 8px;
  margin-left: 12px;
  align-items: center;
}

.header .button-search-mobile svg {
  color: #a2a2a2;
  width: 24px;
  height: 24px;
}

.header .only-desktop {
  display: none;
}

.header .searchbar-mobile {
  display: flex;
  justify-content: center;
  margin-top: 16px;
}

@media screen and (min-width: 480px) {
  .header .content {
    justify-content: space-between;
  }

  .header .only-desktop {
    display: flex;
  }

  .header .button-search-mobile {
    display: none;
  }
  .header .searchbar-mobile {
    display: none;
  }
}
</style>

<script>
import logo from "../assets/logo.png";

export default {
  name: "Header",
  data: () => ({
    logo,
    openSearchBarMobile: false,
  }),
  methods: {
    isMobile() {
      return screen.width <= 480;
    },
    toggleOpenSearchBarMobile() {
      this.openSearchBarMobile = !this.openSearchBarMobile;
    },
  },
  created() {
    this.isMobile();
  },
};
</script>
