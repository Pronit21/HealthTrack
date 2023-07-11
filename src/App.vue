<template>
  <v-app>
    <Header />

    <router-view />
    <v-main>
      <HeroComponent  />
       <AboutUs />
      <PortfolioSection />
      
      <ProjectSection />
      <FitnessCalculator />
      <BmiCalculator />
      
      <GallerySection />
      <ContactUs />

    
      
      <FooterSection />
    </v-main>

  </v-app>
</template>

<script>
import Header from "./components/Header.vue";
import HeroComponent from "./components/HeroComponent.vue";
import AboutUs from "./components/AboutUs.vue";
import PortfolioSection from "./components/PortfolioSection.vue";
import ProjectSection from "./components/ProjectSection.vue";
import GallerySection from "./components/GallerySection";
import ContactUs from "./components/ContactUs";
import FooterSection from "./components/FooterSection";
import BmiCalculator from "./components/BmiCalculator.vue";
import FitnessCalculator from "./components/FitnessCalculator.vue";



import 'boxicons';



export default {
  name: 'App', 
  components: {Header, HeroComponent, PortfolioSection, ProjectSection, GallerySection, ContactUs, FooterSection, AboutUs, BmiCalculator, FitnessCalculator},
  data() {
    return {
      menus: [
        {title:'Home', route:'home'},
        {title:'About us', route:'about-us'},
        {title:'Portfolio', route:'portfolio'},
        {title:'Project', route:'project'},
        {title:'Gallery', route:'gallery'},
        {title:'Contact', route:'contact'}
      ]
    }
  }
};
</script>

<style scoped>
body {
  margin: 0;
}
</style>

