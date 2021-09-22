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
    <h2 class="my-4">Développeur Web Full-Stack</h2>
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

    <h3 class="my-5">Compétences</h3>

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
</style>
