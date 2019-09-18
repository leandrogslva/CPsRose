<template>
    <v-app>
      <header-component></header-component>
      <body-component></body-component>
      <footer-component></footer-component>
    </v-app>
</template>
<script>
import Footer from './components/Footer.vue'
import  Body from './components/Body.vue'
import Header from './components/Header.vue'

export default {
  components: {
    'body-component': Body,
    'header-component': Header,
    'footer-component': Footer,
  }  
}
</script>