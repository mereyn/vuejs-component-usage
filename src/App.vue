<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="selectedComponent = 'appHome'">Home</button>
        <button @click="selectedComponent = 'appAboutUs'">AboutUs</button>
        <button @click="selectedComponent = 'appContactUs'">ContactUs</button>
        <hr>
        <p>{{ selectedComponent }}</p>
        <keep-alive>
          <component :is="selectedComponent">
            <!-- <p>Default Content</p> -->
          </component>
        </keep-alive>
      </div>
    </div>
  </div>
</template>

<script>
import Home from "./components/Home.vue";
import AboutUs from "./components/AboutUs.vue";
import ContactUs from "./components/ContactUs.vue";

export default {
  data: function() {
    return {
      quoteTitle: "Home",
      selectedComponent: "appHome"
    };
  },
  components: {
    appHome: Home,
    appAboutUs: AboutUs,
    appContactUs: ContactUs
  }
};
</script>

<style>
</style>
