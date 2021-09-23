<template>
  <div class="container">
    <b-img
      :src="require('../assets/jmj_img.jpg')"
      alt="Photo de Jean-Marc"
      rounded="circle"
      v-bind="mainProps"
    >
    </b-img>
    <h1 class="mt-5">Jean-Marc Juif</h1>
    <p class="mb-5 h6">
      <b-icon-phone-fill variant="success"></b-icon-phone-fill>
      <a href="tel:06 83 03 85 95">+33 (0)6 83 03 85 95</a>&nbsp;-&nbsp;
      <b-icon-envelope-fill></b-icon-envelope-fill>&nbsp;
      <a href="mailto:jeanmarc.juif@gmail.com">Me contacter par mail</a>
    </p>
    <h2 class="my-4"><strong>Développeur Web Full-Stack</strong></h2>
    <p class="h4">
      Diplomé de la 3wAcadamy en 2015
      <br />
      Diplomé OpenclassRooms parcours développeur web en 2021
    </p>
    <p class="mt-4 social-icons h4">
      <a href="https://github.com/jeanmarcj" target="_blank">
        <b-icon-github class="mr-4"></b-icon-github>
      </a>
      <a href=""><b-icon-linkedin class="mr-4"></b-icon-linkedin></a>
      <a href="https://twitter.com/JeanMarcJ3" target="_blank">
        <b-icon-twitter class="mr-4"></b-icon-twitter>
      </a>
      <a
        href="./CV_JMJ_2021_dev.pdf"
        target="_blank"
        v-b-tooltip.hover
        title="Mon CV en pdf"
      >
        <i class="bi bi-file-earmark-pdf-fill"></i>
      </a>
    </p>

    <h3 class="my-5"><strong>Compétences</strong></h3>

    <!-- Card deck for skills -->
    <b-card-group deck>
      <div v-for="skill in skills" :key="skill.id">
        <b-link :href="skill.link" target="_blank">
          <b-card
            :title="skill.title"
            :img-src="skill.img"
            :img-alt="skill.alt"
            img-top
            tag="article"
            style="max-width: 20rem"
            class="mb-2 text-center"
            bg-variant="dark"
            border-variant="light"
          >
          </b-card>
        </b-link>
      </div>
    </b-card-group>

    <!-- Parcours professionnel -->
    <h3 class="mt-5 mb-2"><strong>Mon parcours professionnel</strong></h3>
    <p class="h4">
      Voici les différentes sociétés avec lesquelles j'ai enrichi mon parcours
      professionnel.
    </p>
    <div class="experience-wrapper d-flex justify-content-between py-5">
      <div class="">
        <!-- colonne gauche -->
        <div class="position-relative d-flex align-items-center">
          <!-- Intérieur Gauche Intérieur Gauche -->
          <div class="experience-vertical-bar bg-danger"></div>
          <div class="experience-circle-round bg-danger"></div>
          <div class="experience-content">
            <p class="experience-content-header font-weight-bold">
              React Participant
            </p>
            <p class="experience-content-header">N17R Incubator, Almaty</p>
            <p class="experience-content-date">Jun 2018 - Aug 2018</p>
          </div>
        </div>

        <!-- Expérice suivante -->
        <div class="position-relative d-flex align-items-center mt-6">
          <!-- Intérieur Gauche Intérieur Gauche -->
          <div class="experience-vertical-bar bg-danger"></div>
          <div class="experience-circle-round bg-danger"></div>
          <div class="experience-content">
            <p class="experience-content-header font-weight-bold">
              Auchan International
            </p>
            <p class="experience-content-header">Le Kremlin Bicêtre</p>
            <p class="experience-content-date">Jun 2018 - Aug 2018</p>
          </div>
        </div>
      </div>
      <div class="">
        <!-- Colonne droite -->
        <div class="position-relative d-flex align-items-center">
          <!-- Intérieur Droit Intérieur Droit -->
          <div class="experience-vertical-bar"></div>
          <div class="experience-circle-round"></div>
          <div class="experience-content">
            <p class="experience-content-header font-weight-bold">
              React Participant
            </p>
            <p class="experience-content-header">N17R Incubator, Almaty</p>
            <p class="experience-content-date">Jun 2018 - Aug 2018</p>
          </div>
        </div>

        <!-- Expérience suivante -->
        <div class="position-relative d-flex align-items-center mt-6">
          <!-- Intérieur Droit Intérieur Droit -->
          <div class="experience-vertical-bar"></div>
          <div class="experience-circle-round"></div>
          <div class="experience-content">
            <p class="experience-content-header font-weight-bold">
              Openclarooms Parcours
            </p>
            <p class="experience-content-header">Paris 15ème</p>
            <p class="experience-content-date">Jun 2018 - Aug 2018</p>
          </div>
        </div>
      </div>
    </div>
    <!-- Experience wrapper end -->
    <!-- Projets réalisés -->
    <h3 class="mt-5 mb-2"><strong>Mes principaux projets</strong></h3>
  </div>
  <!-- container -->
</template>

<script>
// @ is an alias to /src
export default {
  name: "Home",
  data() {
    return {
      mainProps: {
        blank: false,
        blankColor: "#777",
        height: 200,
        width: 200,
      },
      skills: [
        {
          id: 1,
          link: "https://developer.mozilla.org/fr/docs/Web/HTML/Element",
          title: "html5",
          img: "img/logos/html_logo.png",
          alt: "html icon",
        },
        {
          id: 2,
          link: "https://www.css.com/",
          title: "CSS3",
          img: "img/logos/css.svg",
          alt: "CSS icon",
        },
        {
          id: 3,
          link: "https://sass-lang.com",
          title: "Sass",
          img: "img/logos/sass_logo.png",
          alt: "Sass icon",
        },
        {
          id: 4,
          link: "https://developer.mozilla.org/fr/docs/Web/JavaScript",
          title: "JavaScript",
          img: "img/logos/javascript_logo.png",
          alt: "JavaScript icon",
        },
        {
          id: 5,
          link: "https://jquery.com",
          title: "JQuery",
          img: "img/logos/jquery_logo.png",
          alt: "Jquery icon",
        },
        {
          id: 6,
          link: "https://vuejs.org",
          title: "Vue.js",
          img: "img/logos/vuejs_logo.png",
          alt: "Vuejs icon",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
img {
  object-fit: scale-down;
  margin: 0 auto;
}

.social-icons {
  a {
    color: #007bff;
    &:hover {
      color: #dc3545;
    }
  }
}
.card-deck article img {
  height: 5rem;
  width: 10rem;
}
div a {
  color: var(--skill-link);
  &:hover {
    text-decoration: none;
    color: var(--skill-link-hover);
  }
}
// Experience
.experience-wrapper {
  max-width: 640px;
}
.experience-vertical-bar {
  position: absolute;
  width: 0.125rem;
  height: 5rem;
  top: 3.5rem;
  left: 0.2rem;
  background-color: #dc3545;
}
.experience-circle-round {
  height: 0.5rem;
  width: 0.5rem;
  border-radius: 9999px;
  background-color: #dc3545;
}
.experience-content {
  margin-left: 2rem;
  .experience-content-header {
    font-size: 1rem;
    line-height: 1.5rem;
    margin: 0;
  }
  .experience-content-date {
    margin-top: 0.125rem;
    font-size: 0.875rem;
    line-height: 1.25rem;
  }
}
.mt-6 {
  margin-top: 3.5rem;
}
</style>
