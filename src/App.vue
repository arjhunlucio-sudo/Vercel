<script>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
export default {
  components: {
    Navbar,
    Home,
    About,
    Services,
    Contact,
    Footer
  },
  data() {
    return {
      currentPage: 'Home'
    
    }
  },
  methods: {
    changePage(page) {
      this.currentPage = page;
    }
  }
}
</script>

<template>
  <Navbar @goToPage="changePage" />
  <Home v-if="currentPage === 'Home'" />
  <About v-if="currentPage === 'About'" />
  <Services v-if="currentPage === 'Services'"/>
  <Contact v-if="currentPage === 'Contact'"/>
  <Footer/>
</template>
