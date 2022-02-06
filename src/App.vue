<template>
  <div id="app">
    <Header></Header>
    <Home></Home>
    <Footer></Footer>
  </div>
</template>

<script>
import "./styles/global.css";

import Header from "./components/Header";
import Home from "./pages/Home";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Home,
    Footer,
  },
};
</script>


