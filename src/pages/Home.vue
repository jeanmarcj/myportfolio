<template>
  <div class="container">
    <!-- NavBar -->
    <b-navbar toggleable="lg" type="dark" variant="black">
      <b-navbar-brand tag="h1" class="mb-0">Jean-Marc Juif</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <!-- <b-nav-item href="#">Administration</b-nav-item> -->
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item @click="scrollMeTo('parcours')">Mon parcours</b-nav-item>
          <b-nav-item @click="scrollMeTo('portfolio')">
            Mon portfolio
          </b-nav-item>
          <ThemeButton />
          <!-- Drop Down -->
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">FR</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <!-- NavBar End -->
    <b-img
      :src="require('../assets/jmj_img.jpg')"
      alt="Photo de Jean-Marc"
      rounded="circle"
      v-bind="mainProps"
    >
    </b-img>
    <h1 class="mt-5">Jean-Marc Juif</h1>
    <p class="mb-5 h6">
      <b-icon-phone-fill variant="info"></b-icon-phone-fill>
      <a href="tel:06 83 03 85 95">+33 (0)6 83 03 85 95</a>&nbsp;-&nbsp;
      <b-icon-envelope-fill variant="info"></b-icon-envelope-fill>&nbsp;
      <a href="mailto:jeanmarc.juif@gmail.com">Me contacter par mail</a>
    </p>
    <h2 class="my-4"><strong>Développeur Web Full-Stack</strong></h2>
    <p class="h4">
      <a href="img/certificats/Diplôme_3WAcademy.pdf" target="_blank">
        Diplomé de la 3WAcadamy Paris en 2014
      </a>
      <br />
      Certifié Concepteur Web par l'institut F2i de Neuilly en 2015
      <br />
      Diplomé OpenclassRooms Paris parcours développeur web en 2021
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

    <h3 class="my-5"><strong>Mes compétences</strong></h3>

    <h4 class="mb-2">Front-End</h4>
    <!-- Card deck for front skills -->
    <b-card-group deck>
      <div v-for="skill in frontSkills" :key="skill.id">
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

    <h4 class="mt-4 mb-2">Back-End</h4>
    <b-card-group deck>
      <div v-for="skill in backSkills" :key="skill.id">
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

    <h4 class="my-2">Mobile</h4>
    <!-- **************** -->
    <!-- Projets réalisés -->
    <!-- **************** -->
    <h3 class="mt-5 mb-2" ref="portfolio"><strong>Mes réalisations</strong></h3>
    <!-- ********************** -->
    <!-- Parcours professionnel -->
    <!-- ********************** -->
    <h3 class="mt-5 mb-2" ref="parcours">
      <strong>Mon parcours professionnel</strong>
    </h3>
    <p class="h4">
      Voici les différentes sociétés avec lesquelles j'ai enrichi mon parcours
      professionnel.
    </p>
    <div class="experience-wrapper d-flex justify-content-between py-5">
      <!-- colonne gauche -->
      <div class="col-left">
        <!-- Expérience #1 -->
        <Experience
          header="Manager Commerce EEPG (14 marchés)"
          company="Auchan Hypermarchés Le Kremlin Bicêtre"
          period="2015 - Nov 2020"
        >
        </Experience>

        <!-- Expérience #2 -->
        <Experience
          header="Développeur Web"
          company="Auto Entrepreneur"
          period="2014 - 2015"
          class="mt-6"
        >
        </Experience>

        <!-- Expérience #3 -->
        <Experience
          header="Chef des ventes"
          company="Darty Bondy"
          period="2012 - 2013"
          class="mt-6"
        >
        </Experience>

        <!-- Expérience #4 -->
        <Experience
          header="Chef des ventes"
          company="Surcouf Centre Cial Carré Sénart"
          period="2010 - 2012"
          class="mt-6"
        >
        </Experience>

        <!-- Expérience #5 -->
        <Experience
          header="Responsable SAV & Village des techniciens"
          company="Surcouf Centre Cial Belle Epine"
          period="2008 - 2010"
          class="mt-6"
        >
        </Experience>
      </div>
      <!-- Expérience colonne droite -->
      <div class="col-right">
        <!-- Expérience #6 -->
        <Experience
          header="Commercial Expert BtB"
          company="Surcouf Centre Cial Belle Epine"
          period="2002 - 2008"
        >
        </Experience>

        <!-- Expérience #7 -->
        <Experience
          header="Commercial Chef de fabrication"
          company="Victimprim (Studio de création) Asnières"
          period="2002"
          class="mt-6"
        >
        </Experience>
        <!-- Expérience #8 -->
        <Experience
          header="Responsable Centre de profit"
          company="Eurosiège (distribution de meubles) Montreuil"
          period="1999 - 2002"
          class="mt-6"
        >
        </Experience>
        <!-- Expérience #9 -->
        <Experience
          header="Directeur Commercial"
          company="APS - EIM (Import Export de meubles)"
          period="1993 - 1999"
          class="mt-6"
        >
        </Experience>
        <!-- Expérience #10 -->
        <Experience
          header="Chef de Publicité"
          company="Merry - Différence Paris"
          period="1990 - 1993"
          class="mt-6"
        >
        </Experience>
      </div>
      <!-- Experience colonne droite end -->
    </div>
    <!-- Experience wrapper end -->
  </div>
  <!-- container -->
</template>

<script>
// @ is an alias to /src
import Experience from "@/components/Experience.vue";
import ThemeButton from "@/components/ThemeButton.vue";

export default {
  name: "Home",
  components: {
    Experience,
    ThemeButton,
  },
  data() {
    return {
      mainProps: {
        blank: false,
        blankColor: "#777",
        height: 200,
        width: 200,
      },
      frontSkills: [
        {
          id: 1,
          link: "https://git-scm.com",
          title: "Git GitHub",
          img: "img/logos/git_logo.png",
          alt: "Git icon",
        },
        {
          id: 2,
          link: "https://developer.mozilla.org/fr/docs/Web/HTML/Element",
          title: "html5",
          img: "img/logos/html_logo.png",
          alt: "html icon",
        },
        {
          id: 3,
          link: "https://www.css.com/",
          title: "CSS3",
          img: "img/logos/css.svg",
          alt: "CSS icon",
        },
        {
          id: 4,
          link: "https://sass-lang.com",
          title: "Sass",
          img: "img/logos/sass_logo.png",
          alt: "Sass icon",
        },
        {
          id: 5,
          link: "https://getbootstrap.com",
          title: "Bootstrap",
          img: "img/logos/bootstrap_logo.png",
          alt: "Boostrap icon",
        },
        {
          id: 6,
          link: "https://developer.mozilla.org/fr/docs/Web/JavaScript",
          title: "JavaScript",
          img: "img/logos/javascript_logo.png",
          alt: "JavaScript icon",
        },
        {
          id: 7,
          link: "https://jquery.com",
          title: "JQuery",
          img: "img/logos/jquery_logo.png",
          alt: "Jquery icon",
        },
        {
          id: 8,
          link: "https://vuejs.org",
          title: "Vue.js",
          img: "img/logos/vuejs_logo.png",
          alt: "Vuejs icon",
        },
      ],
      backSkills: [
        {
          id: 1,
          link: "https://www.mysql.com/fr/",
          title: "MySQL",
          img: "img/logos/MySql_logo.jpg",
          alt: "MySql icon",
        },
        {
          id: 2,
          link: "https://www.php.net",
          title: "PHP",
          img: "img/logos/php8_logo.png",
          alt: "PHP icon",
        },
      ],
    };
  },
  methods: {
    scrollMeTo(refName) {
      let element = this.$refs[refName];
      let top = element.offsetTop;

      window.scrollTo(0, top);
      console.log(element);
      return;
    },
  },
};
</script>

<style lang="scss">
img {
  object-fit: scale-down;
  margin: 0 auto;
}
#app > div:nth-child(2) > p:nth-child(5) > a:hover {
  color: #dc3545;
}
#app > div:nth-child(2) > p.mb-5.h6 > a:hover {
  color: #dc3545;
}
.social-icons {
  a {
    color: #007bff;
    &:hover {
      color: #dc3545;
    }
  }
}

.card-deck div a {
  text-decoration: none;
  article {
    height: 5rem;
    width: 7rem;
    img {
      height: 2.5rem;
      width: 5rem;
      margin-top: 0.5rem;
    }
    .card-body {
      padding-top: 0.5rem;
      h4 {
        color: var(--skill-link);
        font-size: 0.8rem;
        margin-bottom: 0;
        &:hover {
          color: var(--skill-link-hover);
        }
      }
    }
  }
}

// Experience
.experience-wrapper {
  max-width: 768px;
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
</style>
