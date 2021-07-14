
<template>
  <Navbar/>
  <Content illustration-url="https://picsum.photos/500/300" contentLink="accueil"/>
  <Content illustration-url="https://picsum.photos/500/300" contentLink="presentation"/>
  <Content illustration-url="https://picsum.photos/200/300" contentLink="projets"/>
  <Content illustration-url="https://picsum.photos/600/300" contentLink="contacts"/>
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
    background: linear-gradient(var(--dark), var(--primary));
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
