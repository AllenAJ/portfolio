// theme colors 7075ff, ff7575
<template>
  <v-app>
    <v-content>
      <Home />
      <About />
      <!-- <Skills /> -->
      <Contact />
    </v-content>
      
  </v-app>
</template>
<script>
import Home from './components/Home';
import About from './components/About';
import Contact from './components/Contact';
import config from '../src/conf/data.json';
export default {
  name: 'App',
  components: {
    Home,
    About,
    Contact
  },
  data() {
    return {
      config: config
    }
  },
};
</script>
<style>

  ::selection {
    color: #fff!important;
    background: #7e61ff!important;
  }

  >>>.v-content__wrap{
    margin: 0;
    padding: 0;
    min-height: 0;
  }
</style>