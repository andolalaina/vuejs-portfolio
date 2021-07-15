
<template>
  <Navbar/>
  <Content illustrationFilename="accueil.svg" contentLink="accueil"/>
  <Content illustrationFilename="presentation.svg" contentLink="presentation"/>
  <Content illustrationFilename="projets.svg" contentLink="projets"/>
  <Content illustrationFilename="contacts.svg" contentLink="contacts"/>
</template>


<script>
import Navbar from "./components/Navbar.vue"
import Content from "./components/Content.vue"
export default {
  name: 'App',
  components: {
    Navbar,
    Content
  }
}
</script>

<style>
  :root {
    --dark : #06050F;
    --primary : #9B94DB;
    --green : #188b83;
    --red : #D05353;
    --white : #FEFFFE;

    font-size: 22px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  body {
    background: linear-gradient(var(--dark), var(--primary)) no-repeat;
    height: 400vh;
    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  body::-webkit-scrollbar {
    display: none;
  }

  html {
    scroll-behavior: smooth;
  }
</style>
