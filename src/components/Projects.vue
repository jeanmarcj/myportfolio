<template>
  <div>
    <p class="h4">
      Voici quelques-uns de mes projets favoris.<br />Je les ai développés et
      designés "from scratch".
    </p>
    <div class="project-wrapper" v-for="project in projects" :key="project.id">
      <div class="project-text">
        <div class="project-text-header">
          <a :href="project.projectLink" class="project-text-header-title">
            {{ project.title }}
          </a>
          <p class="project-text-header-subtitle">
            {{ project.subtitle }}
          </p>
        </div>
        <p class="project-text-description text-danger">
          {{ project.description }}
        </p>
        <div class="project-text-techno">
          <p
            class="project-text-techno-description"
            v-for="(tech, index) in project.technos"
            :key="index"
          >
            {{ tech }}
          </p>
        </div>
        <div class="project-text-icons">
          <a
            :href="project.githubLink"
            class="mr-3 position-relative"
            target="_blank"
          >
            <div style="transform: none" v-if="project.githubLink">
              <b-icon-github scale="1.5"></b-icon-github>
            </div>
          </a>
          <a
            :href="project.projectLink"
            class="position-relative"
            target="_blank"
          >
            <div style="transform: none" v-if="project.projectLink">
              <b-icon-box-arrow-in-up-right
                scale="1.5"
                variant="info"
                animation="fade"
              ></b-icon-box-arrow-in-up-right>
            </div>
          </a>
        </div>
      </div>
      <div class="project-img">
        <a :href="project.projectLink">
          <img
            :src="`./img/screenshots/${project.imgLink}`"
            :alt="project.title"
            width="560"
          />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import sourceData from "@/projects.json";

export default {
  name: "Projects",
  data() {
    return {
      projects: sourceData.projects,
    };
  },
};
</script>

<style scoped lang="scss">
.project-wrapper {
  // border-top: 1px solid var(--text-primary-color);
  z-index: 1;
  position: relative;
  //width: 947px;
  //height: 308px;
  margin-top: 3rem;
  .project-text {
    padding: 1.5rem;
    .project-text-header {
      .project-text-header-title {
        font-size: 1.25rem;
        line-height: 1.75rem;
        font-weight: 700;
      }
      .project-text-header-subtitle {
        font-size: 1rem;
        line-height: 1.5rem;
        font-weight: 500;
        margin-bottom: 0;
      }
    }
    .project-text-description {
      font-weight: 500;
      max-width: 30rem;
      border-radius: 0.375rem;
      margin-top: 2rem;
      margin-bottom: 2rem;
      opacity: 1;
      background-color: white;
    }
    .project-text-techno {
      display: flex;
      margin-bottom: 0.5rem;
      .project-text-techno-description {
        font-size: 1rem;
        font-weight: 500;
        line-height: 1.5rem;
        margin-right: 1.25rem;
        &:last-child {
          margin-right: 0;
        }
      }
    }
    .project-text-icons {
      display: flex;
      align-items: center;
      margin-bottom: 0;
    }
  }
  .project-img {
    z-index: -1;
    height: 100%;
    transform: none;
    position: absolute;
    top: 0;
    //height: 308px;
    a {
      img {
        border-radius: 0.6rem;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.25);
        opacity: 0.1;
        width: 100%;
      }
    }
  }
}

@media (min-width: 768px) {
  .project-wrapper {
    margin-top: 5rem;
    // margin-bottom: 2rem;
    .project-img {
      width: 58.33%;
      top: 0.5rem;
      left: 0;
      right: 0;
      a {
        img {
          // border: 1px solid blue;
          opacity: 1;
        }
      }
    }
  }
  .project-text {
    padding: 0;
    .project-text-header {
      text-align: right;
      .project-text-header-title {
        font-size: 1.5rem;
        line-height: 2rem;
      }
      .project-text-header-subtitle {
        font-size: 1.25rem;
        line-height: 1.75rem;
      }
    }
    .project-text-description {
      margin-left: auto;
      text-align: right;
      font-size: 1rem;
      line-height: 1.5rem;
      padding: 1.5rem 2rem;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.25);
    }
    .project-text-techno {
      justify-content: flex-end;
      margin-bottom: 1rem;
      .project-text-techno-description {
        margin-right: 2rem;
        &:last-child {
          margin-right: 0;
        }
      }
    }
    .project-text-icons {
      justify-content: flex-end;
    }
  }
}
@media (min-width: 768px) {
  .project-wrapper {
    margin-top: 7rem;
  }
}
</style>
