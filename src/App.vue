<template>
  <div id="app">
    <Navbar v-if="innerWidth <= 830" />
    <Aside />
    <Start />
    <About />
    <Resume />
    <Service />
    <Portfolio/>
    <Skill />
    <ContactMe />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Aside from './components/Aside.vue'
import Start from './components/Start.vue'
import About from './components/About.vue'
import Resume from './components/Resume.vue'
import Service from './components/Service.vue'
import Portfolio from './components/Portfolio.vue'
import Skill from './components/Skill.vue'
import ContactMe from './components/ContactMe.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,  
    Aside,
    Start,
    About,
    Resume,
    Service,
    Portfolio,
    Skill,
    ContactMe,
    Footer
  },
  data: function () {
      return {
          innerWidth: window.innerWidth,
          showNav: false
      }
    },
    methods: {
      handleResize () {
          this.innerWidth = window.innerWidth;
      }
    },
    mounted() {
     window.addEventListener('resize', this.handleResize);
    },
    beforeUnmount() {
        window.removeEventListener('resize', this.handleResize);
    }
}
</script>

