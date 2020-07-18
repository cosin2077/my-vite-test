<template>
  <div class="app-container">
    <Header />
    <BackgroundImage />
    <img alt="Vue logo" src="./logo.png" />
    <HelloWorld msg="Hello Vue 3.0 + Vite" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import BackgroundImage from "./components/BackgroundImage.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Header,
    BackgroundImage
  }
};
</script>
