<template>
  <v-app>
      <Navbar />
    <v-content>
      <Home />
      <About />
      <Testo />
      <Skills />
      <Projects />
      <Services />
      <ContactNote />
      <ContactForm />
      <Footer />
    </v-content>
  </v-app>
</template>

<script>
import Navbar     from   './components/Navbar'
import Home       from   './components/Home.vue'
import About      from   './components/About.vue'
import Testo      from   './components/Testo.vue'
import Skills     from   './components/Skills.vue'
import Projects   from   './components/Projects.vue'
import Services   from   './components/Services.vue'
import ContactNote    from   './components/ContactNote.vue'
import ContactForm    from   './components/ContactForm.vue'
import Footer    from   './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Home,
    About,
    Testo,
    Skills,
    Projects,
    Services,
    ContactNote,
    ContactForm,
    Footer
  },
  data () {
    return {
      //
    }
  },
  methods: {

  }
}
</script>
<style>
html {
  scroll-behavior: smooth;
}

.theme--light.application {
    background: #fcfcfc;
    color: rgba(0,0,0,0.87);
}

a:hover {
    color: #10437a !important;
    text-decoration: none !important;
}
</style>
