<template>
  <div class="hobbies-wrapper mt-5">
    <b-row class="my-3">
      <!-- #1 -->
      <b-col cols="12" md="4" class="mb-5">
        <article>
          <b-img-lazy
            alt="handball icon"
            width="85%"
            rounded="circle"
            center
            src="./img/logos/handball_red.png"
          >
          </b-img-lazy>
          <h4 class="mt-3">Handball</h4>
          <p>Ex-Joueur International</p>
          <hr />
          <p>
            Section Sport/Etudes de Chartres. Champion d'Europe Sport/Etudes.
            Vice champion de France en Nationale 1. Sportif de haut niveau
            pendant plus de 10ans
          </p>
        </article>
      </b-col>
      <!-- #2 -->
      <b-col cols="12" md="4" class="mb-5">
        <article>
          <b-img-lazy
            alt="tennis icon"
            width="85%"
            rounded="circle"
            center
            src="./img/logos/tennis_red.png"
          >
          </b-img-lazy>
          <h4 class="mt-3">Tennis</h4>
          <p>Pratique en compétition</p>
          <hr />
          <p>
            Joueur classé. Entraînement toutes les semaines. Participation à des
            tournois et championnats les week-end
          </p>
        </article>
      </b-col>
      <!-- #3 -->
      <b-col cols="12" md="4" class="margin-top">
        <article>
          <b-img-lazy
            alt="travel icon"
            width="100%"
            center
            src="./img/logos/travel_red.png"
          >
          </b-img-lazy>
          <h4 class="mt-3">Voyages</h4>
          <p>Séjours à l'étranger</p>
          <hr />
          <p>
            Europe (Italie, Espagne, Grèce, Danemark, Allemage), Etats-Unis
            (Californie, New-York, Miami, Nouvelle Orléans), Canada et Asie du
            Sud Est (Malaisie)
          </p>
        </article>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: "Hobbies",
};
</script>

<style lang="scss">
article > hr {
  background-color: var(--element-secondary-color);
}
.hobbies-wrapper > div > div {
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.25);
}
@media screen and (min-width: 768px) {
  .margin-top {
    margin-top: 0.8rem;
  }
  .hobbies-wrapper > div > div {
    margin-bottom: 0 !important;
    box-shadow: 0 0px 0px rgba(0, 0, 0, 0);
  }
}
</style>
