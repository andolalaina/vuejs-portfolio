
<template>
  <Navbar/>
  <Content illustrationFilename="accueil.svg" contentLink="accueil">
    <div class="title-1">Michael <strong>RANDRIAJAOSON</strong></div>
    <div class="title-2"><strong>Etudiant en Master 2</strong></div>
    <div class="title-3">Electronique Systèmes Informatiques et Intelligence Artificielle (ESIIA-5)</div>
  </Content>
  <Content illustrationFilename="presentation.svg" contentLink="presentation" reversed>

  </Content>
  <Content illustrationFilename="projets.svg" contentLink="projets">

  </Content>
  <Content illustrationFilename="contacts.svg" contentLink="contacts">

  </Content>
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
    background: linear-gradient(#06050F, #18143E, #2B236C, #4338A8, #7066CC ) no-repeat;
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

<style scoped>
  .title-1 {
    font-size: 2.35rem;
    margin: 1.15rem 0;
  }
  .title-2 {
    font-size: 1.45rem;
  }
  .title-3 {
    font-size: 1.18rem;
  }
</style>