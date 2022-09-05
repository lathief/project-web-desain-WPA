<template>
  <v-app>
    <Header/>
    <v-main>
      <HeroComponent/>
      <Design/>
      <About/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header.vue';
import HeroComponent from './components/HeroComponent.vue';
import About from './components/About.vue';
import Design from './components/Design.vue';
import Footer from './components/Footer.vue';

export default {
    name: "App",
    data() {
        return {
            
        };
    },
    components: { Header, HeroComponent, About, Design, Footer }
};
</script>