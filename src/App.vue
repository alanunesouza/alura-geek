<template>
  <v-app>
    <v-main class="container-app">
      <Header />
      <div class="banner-container">
        <v-img class="banner" :src="banner"></v-img>
        <div class="content">
          <h1>Dezembro Promocional</h1>
          <p class="font-weight-small mt-1">
            Produtos selecionados com 33% de desconto
          </p>
          <v-btn width="133" elevation="2" color="primary" class="mt-2">
            Ver Consoles
          </v-btn>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<style>
.container-app {
  width: 100%;
  height: 100%;
  margin: 0px auto;
}

.container-app .banner-container {
  position: relative;
}

.container-app .banner-container .content {
  bottom: 32px;
  left: 32px;
  position: absolute;
}

.container-app .banner-container .content h1,
p {
  color: #fff;
}

@media screen and (max-width: 768px) {
  .container-app .banner {
    height: 192px;
  }

  .container-app .banner img {
    object-fit: cover;
  }
}
</style>

<script>
import Header from "./components/Header.vue";
import banner from "./assets/banner-image.png";

export default {
  name: "App",
  components: {
    Header,
  },

  data: () => ({
    banner,
  }),
};
</script>
