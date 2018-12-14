<template>
  <div>
    <Navbar></Navbar>
    <nuxt/>
    <Footer></Footer>
  </div>
</template>

<script>
  import Navbar from '~/components/Navbar.vue'
  import Footer from '~/components/Footer.vue'

  export default {
    head () {
      return {
        script: [
          { src: 'https://use.fontawesome.com/releases/v5.0.6/js/all.js' }
        ],
        link: [
          { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Pacifico|Roboto' }
        ]
      }
    },
    components: {
      Navbar, Footer
    },
  }
</script>

