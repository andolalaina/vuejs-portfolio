
<template>
  <Navbar/>
  <Content illustrationFilename="accueil.svg" contentLink="accueil">
    <div class="title-1">Michael <strong>RANDRIAJAOSON</strong></div>
    <div class="title-2"><strong>Etudiant en Master 2</strong></div>
    <div class="title-3">Electronique Systèmes Informatiques et Intelligence Artificielle (ESIIA-5)</div>
  </Content>
  <Content illustrationFilename="presentation.svg" contentLink="presentation">
    <Scroller width="100%" height="60vh">
      <Degree v-for="course in courses" :key="course.id" :date="course.date" :title="course.title" :course="course.description" :institution="course.institution" />
    </Scroller>
  </Content>
  <Content illustrationFilename="projets.svg" contentLink="projets" reversed>
    <Scroller width="100%" height="60vh">
      <Card v-for="project in projects" :key="project.id" :illustrationFilename="project.illustration" :title="project.title" :link="project.link" :technos="project.technos" />
    </Scroller>
  </Content>
  <Content illustrationFilename="contacts.svg" contentLink="contacts">
  </Content>
</template>


<script>
import Navbar from "./components/Navbar.vue"
import Content from "./components/Content.vue"
import Degree from "./components/Degree.vue"
import Scroller from "./components/Scroller.vue"
import Card from "./components/Card.vue"

export default {
  name: 'App',
  components: {
    Navbar,
    Content,
    Degree,
    Scroller,
    Card
  },
  data() {
    return {
      courses : [
        {
          id : 1,
          date : "2022",
          title : "Diplôme de Master",
          description : "Master en Electronique Systèmes Informatiques et Intelligence Artificielle",
          institution : "Institut Supérieur Polytechnique de Madagascar (ISPM), Antsobolo, Antananarivo"
        },
        {
          id : 2,
          date : "2020",
          title : "Diplôme de Licence",
          description : "Licence en Electronique Systèmes Informatiques et Intelligence Artificielle",
          institution : "Institut Supérieur Polytechnique de Madagascar (ISPM), Antsobolo, Antananarivo"
        },
        {
          id : 2,
          date : "2019 - 2020",
          title : "Stage de trois (03) mois",
          description : "Stage en tant qu'administrateur systèmes et réseaux",
          institution : "Bolloré Madagascar, Tanjombato, Antananarivo"
        },
        {
          id : 3,
          date : "2016",
          title : "Baccalauréat",
          description : "Série D, avec mention",
          institution : "College Saint Michel, Amparibe, Antananarivo"
        }
      ],
      projects : [
        {
          id : 1,
          illustration : "html-visit-card.png",
          title : "Visit Card",
          link : "https://andolalaina.github.io/w1-visit-card/",
          technos : [
            {
              id : 1,
              logo : "html.png"
            },
            {
              id : 2,
              logo : "css.png"
            },
          ]
        },
        {
          id : 1,
          illustration : "html-visit-card.png",
          title : "Visit Card",
          link : "https://andolalaina.github.io/w1-visit-card/",
          technos : [
            {
              id : 1,
              logo : "html.png"
            },
            {
              id : 2,
              logo : "css.png"
            },
          ]
        },
        {
          id : 1,
          illustration : "html-visit-card.png",
          title : "Visit Card",
          link : "https://andolalaina.github.io/w1-visit-card/",
          technos : [
            {
              id : 1,
              logo : "html.png"
            },
            {
              id : 2,
              logo : "css.png"
            },
          ]
        },
        {
          id : 1,
          illustration : "html-visit-card.png",
          title : "Visit Card",
          link : "https://andolalaina.github.io/w1-visit-card/",
          technos : [
            {
              id : 1,
              logo : "html.png"
            },
            {
              id : 2,
              logo : "css.png"
            },
          ]
        },
      ]
    }
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