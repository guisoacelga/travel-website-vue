<template>
  <div id="app">
    <Header v-model="searchText" />
    <main>
      <div class="container">
        <router-view :searchText="searchText"></router-view>
      </div>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Footer
  },
  data() {
    return {
      searchText: ""
    };
  }
};
</script>

<style>
@font-face {
  font-family: "GT Eesti";
  src: url("assets/fonts/GT-Eesti-Pro-Display-Regular.woff2") format("woff");
}

* {
  font-family: "GT Eesti", Arial, Helvetica, sans-serif;
}

header {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 2;
}

main {
  margin-top: 60px;
  z-index: 1;
}

main > .container .card {
  min-height: 490px;
}

.mt-20 {
  margin-top: 20px;
}

.btn {
  letter-spacing: 1px;
}

.card .btn {
  position: absolute;
  bottom: 20px;
}

footer {
  height: 80px;
  margin-top: 50px;
}

footer > .container,
footer .row {
  height: 100%;
}

.iconsFooter {
  color: #007bff;
  margin-left: 10px;
  cursor: pointer;
}
</style>
