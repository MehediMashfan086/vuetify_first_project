<template>
  <v-app>
    <Header></Header>

    <v-main>
      <!-- Hero Section -->
      <HeroComponent/>

      <!-- About Us Section -->
      <Aboutus/>

      <!-- Portfolio Section -->
      <Portfolio />

      <!-- Portfolio Section -->
      <Project/>

      <!-- Gallery Section -->
      <Gallery />

      <!-- Contact Us Section -->
      <Contactus />

      <!-- Footer Section -->
      <Footer />
    </v-main>
  </v-app>
</template>

<script>

import Header from "./components/Header"
import HeroComponent from "./components/HeroComponent.vue"
import Aboutus from "./components/Aboutus.vue";
import Portfolio from "./components/Portfolio.vue";
import Project from "./components/Project.vue";
import Gallery from "./components/Gallery.vue";
import Contactus from "./components/Contactus.vue";
import Footer from "./components/Footer.vue";
export default {
  name: 'App',
  components: { Header, HeroComponent, Aboutus, Portfolio, Project, Gallery, Contactus, Footer },
  data() {
            return {
                menus: [
                    {title:'Home',      route:'home'},
                    {title:'About Us',  route:'about-us'},
                    {title:'Protfolio', route:'protfolio'},
                    {title:'Project',   route:'project'},
                    {title:'Gallery',   route:'gallery'},
                    {title:'Contact',   route:'contact'},
      ]
    }
  }
};
</script>
