<template>
  <div class="container">
    <!-- NavBar -->
    <b-navbar toggleable="lg" type="dark" variant="black" ref="navBarTop">
      <!-- <b-navbar-brand tag="h1" class="mb-0">Jean-Marc Juif</b-navbar-brand> -->
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <!-- <b-nav-item href="#">Administration</b-nav-item> -->
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item @click="scrollMeTo('portfolio')"> Portfolio</b-nav-item>
          <b-nav-item @click="scrollMeTo('parcours')">Parcours</b-nav-item>
          <b-nav-item @click="scrollMeTo('formations')">Formations</b-nav-item>
          <b-nav-item @click="scrollMeTo('recommandations')">
            Recommandations
          </b-nav-item>
          <b-nav-item @click="scrollMeTo('loisirs')">
            Centre d'intérêts
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
    <!-- Header -->
    <header>
      <b-row class="align-items-center">
        <b-col cols="12" md="3">
          <b-img
            :src="require('../assets/jmj_img.jpg')"
            alt="Photo de Jean-Marc Juif"
            rounded="circle"
            v-bind="mainProps"
          >
          </b-img>
        </b-col>
        <b-col cols="12" md="9">
          <p class="lead ml-sm-0 ml-md-5">
            <i>
              "Je cherche un poste de développeur web full-stack.<br />Tenacité,
              confiance, rigueur et persévérance sont mes valeurs.<br />Je
              développe des projets en JavaScript, PHP et Swift. J'utilise des
              framework reconnus comme Xcode, Symfony et Vue.JS"
            </i>
          </p>
        </b-col>
      </b-row>
    </header>
    <h1 class="mt-5">Jean-Marc Juif</h1>
    <p class="mb-5 h6">
      <b-icon-phone-fill variant="info"></b-icon-phone-fill>
      <a href="tel:06 83 03 85 95">+33 (0)6 83 03 85 95</a>&nbsp;-&nbsp;
      <b-icon-envelope-fill variant="info"></b-icon-envelope-fill>&nbsp;
      <a href="mailto:jeanmarc.juif@gmail.com">Me contacter par mail</a>
    </p>
    <h2 class="my-5"><strong>Développeur Web Full-Stack</strong></h2>
    <section class="h4">
      <div class="my-1">
        <a href="./img/certificats/3wAcademy.pdf" target="_blank">
          Diplomé Concepteur & Intégrateur Web par la 3WAcadamy Paris en 2014
        </a>
      </div>
      <div class="my-1">
        <a href="./img/certificats/F2I_Attestation_Stage.pdf" target="_blank">
          Certifié Concepteur Web par l'Institut Européen F2i de Vincennes en
          2015
        </a>
      </div>
      <div>
        <a
          href="./img/certificats/OC_Certificat de scolarité JMJ.pdf"
          target="_blank"
        >
          Diplomé OpenclassRooms Paris parcours Développeur Web en 2021
        </a>
      </div>
    </section>
    <section id="socials">
      <p class="mt-4 social-icons h4">
        <a href="https://github.com/jeanmarcj" target="_blank">
          <b-icon-github class="mr-4"></b-icon-github>
        </a>
        <a
          href="https://www.linkedin.com/in/jean-marc-juif-a7bb542"
          target="_blank"
        >
          <b-icon-linkedin class="mr-4"></b-icon-linkedin>
        </a>
        <a href="https://twitter.com/JeanMarcJ3" target="_blank">
          <b-icon-twitter class="mr-4"></b-icon-twitter>
        </a>
        <a
          href="./JM_Juif_Dev_Web_FullStack.pdf"
          target="_blank"
          v-b-tooltip.hover
          title="Mon CV en pdf"
        >
          <i class="bi bi-file-earmark-pdf-fill"></i>
        </a>
      </p>
    </section>
    <!-- *********** -->
    <!-- Compétences -->
    <!-- *********** -->
    <section id="skills">
      <h3 class="my-5"><strong>Compétences</strong></h3>
      <h4 class="mb-2">Front-End</h4>
      <!-- front skills -->
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
      <!-- Back-End skills -->
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
      <!-- Mobile Skills -->
      <h4 class="mt-4 mb-2">Mobile</h4>
      <b-card-group deck>
        <div
          v-for="skill in mobileSkills"
          :key="skill.id"
          v-b-tooltip.hover.v-primary
          v-b-tooltip.hover.html="skill.tipData"
        >
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
    </section>
    <div class="text-right my-5">
      <b-link @click="scrollMeTo('navBarTop')">
        <b-icon-arrow-up-square-fill
          variant="danger"
          font-scale="1.5"
          animation="cylon-vertical"
        >
        </b-icon-arrow-up-square-fill>
      </b-link>
    </div>
    <!-- **************** -->
    <!-- Projets réalisés -->
    <!-- **************** -->
    <section id="projects">
      <h3 class="mt-5 mb-2" ref="portfolio">
        <strong>Mes projets</strong>
      </h3>
      <Projects />
    </section>
    <div class="text-right my-5">
      <b-link @click="scrollMeTo('navBarTop')">
        <b-icon-arrow-up-square-fill
          variant="danger"
          font-scale="1.5"
          animation="cylon-vertical"
        >
        </b-icon-arrow-up-square-fill>
      </b-link>
    </div>
    <!-- ********************** -->
    <!-- Parcours professionnel -->
    <!-- ********************** -->
    <h3 class="mt-5 mb-2" ref="parcours">
      <strong>Parcours professionnel</strong>
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
          company="Auchan Retail France Le Kremlin Bicêtre"
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
    <div class="text-right my-5">
      <b-link @click="scrollMeTo('navBarTop')">
        <b-icon-arrow-up-square-fill
          variant="danger"
          font-scale="1.5"
          animation="cylon-vertical"
        >
        </b-icon-arrow-up-square-fill>
      </b-link>
    </div>
    <!-- ********** -->
    <!-- Formations -->
    <!-- ********** -->
    <section id="learning">
      <h3 class="mt-5 mb-2" ref="formations">
        <strong>Diplômes et Formations</strong>
      </h3>
      <Formations
        header="Développeur Web"
        company="OpenclassRooms Paris"
        date="2021"
        description="Intégration HTML et CSS - JavaScript - Optimisation SEO. 7 projets réalisés (site e-commerce en JavaScript, développement d'un back-end sécurisé en NodeJS, création d’une application complète de messagerie en JavaScript, SQL, en NodeJS (Express) et VueJS. 29 certifications OpenclassRooms. Titre professionnel de niveau 5."
      >
      </Formations>
      <Formations
        header="Développeur d'applications Web"
        company="Institut F2I Vincennes"
        date="2014 - 2015"
        description="UML - Gestion de projets (ITIL) - JavaScript - MySQL - PHP - Symfony - .net - Apple Swift"
      >
      </Formations>
      <Formations
        header="Intégrateur Développeur Web"
        company="3W Academy Paris"
        date="2014"
        description="HTML - CSS - JavaScript - JQuery - PHP - MySql - WordPress, Drupal, PrestaShop - Symfony. Développement de 5 projets."
      >
      </Formations>
      <Formations
        header="BTS Communication & Actions Publicitaires"
        company="Ecole Supérieure de Publicité - Paris"
        description="Formation Chef de Publicité"
      >
      </Formations>
      <Formations header="Bac B" company="Sciences Economiques & Sociales">
      </Formations>
    </section>
    <div class="text-right my-5">
      <b-link @click="scrollMeTo('navBarTop')">
        <b-icon-arrow-up-square-fill
          variant="danger"
          font-scale="1.5"
          animation="cylon-vertical"
        >
        </b-icon-arrow-up-square-fill>
      </b-link>
    </div>
    <!-- *************** -->
    <!-- Recommandations -->
    <!-- *************** -->
    <h3 class="my-5" ref="recommandations">
      <strong>Recommandations</strong>
    </h3>
    <Quotes />
    <div class="text-right my-5">
      <b-link @click="scrollMeTo('navBarTop')">
        <b-icon-arrow-up-square-fill
          variant="danger"
          font-scale="1.5"
          animation="cylon-vertical"
        >
        </b-icon-arrow-up-square-fill>
      </b-link>
    </div>
    <!-- ******* -->
    <!-- Centres d'intérêts -->
    <!-- ******* -->
    <section>
      <h3 class="mt-5 mb-2" ref="loisirs">
        <strong>Centres d'intérêts</strong>
      </h3>
      <Hobbies />
    </section>
    <div class="text-right my-5">
      <b-link @click="scrollMeTo('navBarTop')">
        <b-icon-arrow-up-square-fill
          variant="danger"
          font-scale="1.5"
          animation="cylon-vertical"
        >
        </b-icon-arrow-up-square-fill>
      </b-link>
    </div>
    <!-- ****** -->
    <!-- Footer -->
    <!-- ****** -->
    <Footer />
  </div>
  <!-- container -->
</template>

<script>
// @ is an alias to /src
import ThemeButton from "@/components/ThemeButton.vue";
import Projects from "@/components/Projects.vue";
import Experience from "@/components/Experience.vue";
import Formations from "@/components/Formations.vue";
import Quotes from "@/components/Quotes";
import Hobbies from "@/components/Hobbies";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Experience,
    ThemeButton,
    Projects,
    Formations,
    Quotes,
    Hobbies,
    Footer,
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
          alt: "Git logo",
        },
        {
          id: 2,
          link: "https://developer.mozilla.org/fr/docs/Web/HTML/Element",
          title: "html5",
          img: "img/logos/html_logo.png",
          alt: "html logo",
        },
        {
          id: 3,
          link: "https://www.css.com/",
          title: "CSS3",
          img: "img/logos/css.svg",
          alt: "CSS logo",
        },
        {
          id: 4,
          link: "https://sass-lang.com",
          title: "Sass",
          img: "img/logos/sass_logo.png",
          alt: "Sass logo",
        },
        {
          id: 5,
          link: "https://getbootstrap.com",
          title: "Bootstrap",
          img: "img/logos/bootstrap_logo.png",
          alt: "Boostrap logo",
        },
        {
          id: 6,
          link: "https://developer.mozilla.org/fr/docs/Web/JavaScript",
          title: "JavaScript",
          img: "img/logos/javascript_logo.png",
          alt: "JavaScript logo",
        },
        {
          id: 7,
          link: "https://jquery.com",
          title: "JQuery",
          img: "img/logos/jquery_logo.png",
          alt: "Jquery logo",
        },
        {
          id: 8,
          link: "https://vuejs.org",
          title: "Vue.js",
          img: "img/logos/vuejs_logo.png",
          alt: "Vuejs logo",
        },
      ],
      backSkills: [
        {
          id: 1,
          link: "https://www.mysql.com/fr/",
          title: "MySQL",
          img: "img/logos/MySql_logo.jpg",
          alt: "MySql logo",
        },
        {
          id: 2,
          link: "https://www.mongodb.com/fr-fr",
          title: "mongoDB",
          img: "img/logos/mongoDB_logo.png",
          alt: "mongoDB logo",
        },
        {
          id: 3,
          link: "./img/certificats/OC_Certificat_API_REST.pdf",
          title: "API Rest",
          img: "img/logos/APIRest_logo.png",
          alt: "API Rest logo",
        },
        {
          id: 4,
          link: "https://www.php.net",
          title: "PHP",
          img: "img/logos/php8_logo.jpeg",
          alt: "PHP logo",
        },
        {
          id: 5,
          link: "https://wordpress.com/fr/",
          title: "WordPress",
          img: "img/logos/wordpress_logo.png",
          alt: "WordPress logo",
        },
        {
          id: 6,
          link: "https://www.doctrine-project.org/index.html",
          title: "Doctrine",
          img: "img/logos/doctrine_logo.png",
          alt: "Doctrine logo",
        },
        {
          id: 7,
          link: "https://symfony.com/",
          title: "Symfony",
          img: "img/logos/symfony_logo.png",
          alt: "Doctrine logo",
        },
        {
          id: 8,
          link: "https://nodejs.org/fr/",
          title: "NodeJS",
          img: "img/logos/nodejs_logo.png",
          alt: "Nodejs logo",
        },
        {
          id: 9,
          link: "https://sequelize.org/",
          title: "Sequelize",
          img: "img/logos/sequelize_logo.png",
          alt: "Sequelize ORM logo",
        },
        {
          id: 10,
          link: "https://expressjs.com/fr/",
          title: "ExpressJS",
          img: "img/logos/express_logo.png",
          alt: "Sequelize ORM logo",
        },
      ],
      mobileSkills: [
        {
          id: 1,
          link: "https://www.apple.com/fr/swift/",
          title: "iOS Swift",
          img: "img/logos/swift_logo.png",
          alt: "Swift logo",
          tipData: {
            title:
              "iOS Swift les fondamentaux. <a href='./img/certificats/OC_Certificat_Fondamentaux_Swift.pdf' target='_blank'>Voir le certificat</a>",
            html: true,
          },
        },
        {
          id: 2,
          link: "https://www.apple.com/fr/swift/",
          title: "Swift POO",
          img: "img/logos/swift_logo.png",
          alt: "Swift logo",
          tipData: {
            title:
              "iOS Swift Programmation Orientée Objet.<br/><a href='./img/certificats/OC_Certificat_Swift_POO.pdf' target='_blank'>Voir le certificat</a>",
            html: true,
          },
        },
        {
          id: 3,
          link: "https://www.apple.com/fr/swift/",
          title: "iOS",
          img: "img/logos/ios_logo.png",
          alt: "iOS logo",
          tipData: {
            title:
              "iOS Introduction.<br /><a href='./img/certificats/OC_Certificat_intro_IOS.pdf' target='_blank'>Voir le certificat</a>",
            html: true,
          },
        },
        {
          id: 4,
          link: "https://www.apple.com/fr/swift/",
          title: "iOS MVC",
          img: "img/logos/ios_logo.png",
          alt: "iOS logo",
          tipData: {
            title:
              "Créer une application iPhone MVC.<br /><a href='./img/certificats/OC_Certificat_IOS_APP_MVC.pdf' target='_blank'>Voir le certificat</a>",
            html: true,
          },
        },
        {
          id: 5,
          link: "https://www.apple.com/fr/swift/",
          title: "Responsive",
          img: "img/logos/ios_logo.png",
          alt: "iOS logo",
          tipData: {
            title:
              "Créer une application iPhone Responsive.<br /><a href='./img/certificats/OC_Certificat_IOS_App_Responsive.pdf' target='_blank'>Voir le certificat</a>",
            html: true,
          },
        },
        {
          id: 6,
          link: "https://www.apple.com/fr/swift/",
          title: "Navigation",
          img: "img/logos/ios_logo.png",
          alt: "iOS logo",
          tipData: {
            title:
              "Gérez la navigation et les formulaires en iOS.<br /><a href='./img/certificats/OC_Certificat_iOS_Navigation.pdf' target='_blank'>Voir le certificat</a>",
            html: true,
          },
        },
      ],
    };
  },
  methods: {
    scrollMeTo(refName) {
      let element = this.$refs[refName];
      let top = element.offsetTop;

      window.scrollTo(0, top);
      // console.log(element);
      return;
    },
  },
};
</script>

<style lang="scss">
.navbar-dark .navbar-toggler-icon {
  background-color: var(--accent-color);
}
img {
  object-fit: scale-down;
  margin: 0 auto;
}
a:hover {
  text-decoration: none !important;
  color: #dc3545 !important;
}
.social-icons {
  a {
    color: #007bff;
  }
}

.card-deck div a {
  text-decoration: none;
  article {
    height: 5rem;
    width: 7rem;
    border-radius: 1.3rem;
    &:hover {
      border-color: #dc3545 !important;
    }
    img {
      height: 2.5rem;
      width: 5rem;
      margin-top: 0.5rem;
    }
    .card-body {
      padding-top: 0.5rem;
      h4 {
        color: var(--skill-link) !important;
        font-size: 0.8rem;
        margin-bottom: 0;
        &:hover {
          color: var(--skill-link-hover) !important;
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
  background: no-repeat;
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
