<template>
  <section id="about">
    <!-- Quote #1 -->
    <div
      class="
        quotes-wrapper
        d-flex
        justify-content-center justify-content-md-start
      "
    >
      <blockquote
        class="blockquote"
        :style="{
          'background-image':
            'url(' + require('../assets/quotation-mark-symbol.png') + ')',
        }"
      >
        <p class="lead">
          <i>
            Projet responsive design. Sémantique html OK. Validation w3c.
            Présentation fluide et structurée. Tous les choix ont été justifiés.
            Chaque point du brief a été clairement expliqué. Bonne compréhension
            de l'intégration d'une maquette. Bonne compréhension de Git.
          </i>
        </p>
        <footer class="blockquote-footer text-center">
          Aurélien Morvan - Evaluateur et Mentor chez OpenclassRooms
        </footer>
      </blockquote>
    </div>
    <!-- Quote #2 -->
    <div
      class="
        quotes-wrapper
        d-flex
        justify-content-center justify-content-md-end
      "
    >
      <blockquote
        class="blockquote"
        :style="{
          'background-image':
            'url(' + require('../assets/quotation-mark-symbol.png') + ')',
        }"
      >
        <p class="lead">
          <i>
            L'aspect visuel correspond à la maquette sur écran mobile. Le projet
            est responsif sur mobile, tablette et desktop. Très bon travail,
            l'étudiant a le souci du détail. Utilisation de BEM et de
            l'architecture 7-1 (SASS). Très bonnes explications. Très bonne
            présentation, les explications sont claires, les réponses aux
            questions montrent que l'étudiant a maîtrisé les notions abordées
            dans le projet. Félicitations.
          </i>
        </p>
        <footer class="blockquote-footer text-center">
          Wilfried Mambou - Evaluateur et Mentor chez OpenclassRooms
        </footer>
      </blockquote>
    </div>
    <!-- Quote #3 -->
    <div
      class="
        quotes-wrapper
        d-flex
        justify-content-center justify-content-md-start
      "
    >
      <blockquote
        class="blockquote"
        :style="{
          'background-image':
            'url(' + require('../assets/quotation-mark-symbol.png') + ')',
        }"
      >
        <p class="lead">
          <i>
            On retrouve dans le rapport d'analyse SEO, des recommandations liées
            à l'accessibilité. Pour chaque problème identifié on retrouve la
            bonne pratique à adopter, l'explication du problème et la référence.
            Le code est correctement indenté et passe la validation W3C. Le
            rapport d'optimisation montre les améliorations. Tous les documents
            sont présents, complets et correctement rédigés. Soutenance où tout
            est dit et bien justifié.
          </i>
        </p>
        <footer class="blockquote-footer text-center">
          Florent Boutin - Evaluateur et Mentor chez OpenclassRooms
        </footer>
      </blockquote>
    </div>
    <!-- Quote #4 -->
    <div
      class="
        quotes-wrapper
        d-flex
        justify-content-center justify-content-md-end
      "
    >
      <blockquote
        class="blockquote"
        :style="{
          'background-image':
            'url(' + require('../assets/quotation-mark-symbol.png') + ')',
        }"
      >
        <p class="lead">
          <i>
            Points forts : code JavaScript modulaire, design travaillé et
            réalisé, travail de qualité professionnelle. Très bonne présentation
            orale : claire, structurée et fluide. Très bonne implication dans la
            mission. Bravo pour cet excellent travail.
          </i>
        </p>
        <footer class="blockquote-footer text-center">
          Olivier Elophe - Evaluateur et Mentor chez OpenclassRooms
        </footer>
      </blockquote>
    </div>
    <!-- Quote #5 -->
    <div
      class="
        quotes-wrapper
        d-flex
        justify-content-center justify-content-md-start
      "
    >
      <blockquote
        class="blockquote"
        :style="{
          'background-image':
            'url(' + require('../assets/quotation-mark-symbol.png') + ')',
        }"
      >
        <p class="lead">
          <i>
            Les données sont stockées de manière sécurisée dans la base de
            données. Le modèle logique est implémenté. Les opérations de CRUD
            sont mises en œuvre. Bonne présentation et explication du projet.
          </i>
        </p>
        <footer class="blockquote-footer text-center">
          Samuel Dongmo - Evaluateur et Mentor chez OpenclassRooms
        </footer>
      </blockquote>
    </div>
    <!-- Quote #6 -->
    <div
      class="
        quotes-wrapper
        d-flex
        justify-content-center justify-content-md-end
      "
    >
      <blockquote
        class="blockquote"
        :style="{
          'background-image':
            'url(' + require('../assets/quotation-mark-symbol.png') + ')',
        }"
      >
        <p class="lead">
          <i>
            L'application web contient les logos et la gamme de couleurs fournis
            par le client. La page est conforme aux normes WCAG. L'utilisateur
            peut faire des requêtes de données depuis SQL. Points forts :
            l'ajout des "SLUGs" est une très bonne idée. Bonne présentation, tu
            maîtrises bien ton code. Bon courage pour ta future vie
            professionnelle.
          </i>
        </p>
        <footer class="blockquote-footer text-center">
          Christophe Lopez - Evaluateur et Mentor chez OpenclassRooms
        </footer>
      </blockquote>
    </div>
  </section>
</template>

<script>
export default {
  name: "Quotes",
};
</script>

<style scoped lang="scss">
#about {
  .quotes-wrapper {
    margin-bottom: 3rem;
    blockquote {
      width: 100%;
      border-radius: 0.8rem;
      background-color: var(--background-color-inverse);
      background-position: 5% 5%;
      background-repeat: no-repeat;
      background-size: 5%;
      color: var(--accent-color);
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.8);
      p {
        padding: 2.5em 3rem 0rem 3rem;
      }
      p > i {
        color: var(--accent-color);
      }
      footer {
        padding: 2rem;
      }
    }
  }
  @media (min-width: 768px) {
    .quotes-wrapper {
      blockquote {
        width: 65%;
      }
    }
  }
}
</style>
