
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
  <Content illustrationFilename="projets.svg" contentLink="projets">
    <Scroller width="100%" height="60vh">
      <Card v-for="project in projects" :key="project.id" :illustrationFilename="project.illustration" :title="project.title" :link="project.link" :technos="project.technos" />
    </Scroller>
  </Content>
  <Content illustrationFilename="contacts.svg" contentLink="contacts" reversed>
    <h2>Réseaux Sociaux</h2>
    <p class="credential">
      <img src="./assets/social-logos/github.svg" alt="github logo">
      <a href="http://www.github.com/andolalaina" target="_blank">Andolalaina</a>
    </p>
    <p class="credential">
      <img src="./assets/social-logos/linkedin.svg" alt="linkedin logo">
      <a href="https://www.linkedin.com/in/michael-randriajaoson-9b5ba318b/" target="_blank">Michael <strong>RANDRIAJAOSON</strong></a>
    </p>
    <h2>Formulaire de contact</h2>
    <form action="" method="get" class="form">
      <label for="mail">Votre adresse e-mail</label>
      <input type="mail" name="mail" id="mail">
      <label for="message">Votre message</label>
      <textarea name="message" cols="30" rows="10" id="message"></textarea>
      <input type="submit" value="Envoyer" class="btn btn-dark">
    </form>
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
          id : 3,
          date : "2019 - 2020",
          title : "Stage de trois (03) mois",
          description : "Stage en tant qu'administrateur systèmes et réseaux",
          institution : "Bolloré Madagascar, Tanjombato, Antananarivo"
        },
        {
          id : 4,
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
          id : 2,
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
          id : 3,
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
          id : 4,
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

    font-size: 18px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  @media screen and (min-width: 1367px) {
    :root {
      font-size: 22px;
    }
  }

  body {
    background: linear-gradient(#06050F, #18143E, #2B236C, #4338A8, #7066CC ) no-repeat;
    height: 400vh;
    overflow: hidden;
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

  h2 {
    margin: .5rem 0;
  }
  .credential {
    font-size: .81rem;
    display: flex;
    align-items: center;
    margin: .5rem;
  }
  .credential>a {
    color: var(--white);
    text-decoration: none;
    margin-left: 1rem;
  }
  .form {
    display: flex;
    flex-flow: column;
  }
  .form>input[type="mail"] {
    border: 0;
    width: 30%;
    height: 1.25rem;
    border-radius: 3px;
    margin: .5rem 0;
    font-size: .8rem;
  }
  .btn {
    padding: .25rem 2rem;
    margin: .5rem 0;
    font-size: 1rem;
    max-width: fit-content;
    cursor: pointer;
    border-radius: 5px;
  }
  .btn-dark {
    color: var(--white);
    background-color: var(--dark);
  }
</style>