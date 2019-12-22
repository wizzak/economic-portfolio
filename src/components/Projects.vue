/* eslint-disable quotes */
<template>
  <div id="projects-wrapper">
    <div id="projects-headline">
      <h2>Projekte</h2>
      <p>Eine Auswahl meiner Projekte an denen ich mitgearbeite habe.</p>
    </div>
    <div id="projects-items">
      <div class="projects-item" v-for="(value, name) in projects">
        <div class="projects-image-wrapper">
          <img v-bind:src="value.url" alt="project_1" />
        </div>
        <span class="projects-name">{{value.name}}</span>
        <span class="projects-customer">{{value.customer}}</span>
      </div>
    </div>
    <div class="projects-slider-wrapper">
      <div class="projects-slider">
        <div class="slider-arrows">
          <div class="slider-arrow-up">
            <img src="..\assets\icons\angle-up-light.svg" alt="angle-up" />
          </div>
          <div class="slider-arrow-down">
            <img src="..\assets\icons\angle-down-light.svg" alt="angle-down" />
          </div>
        </div>
        <div class="projects-slider-items">
          <div
            class="projects-slider-item-wrapper"
            :style="{'background-image': 'url(' + value.url + ')'}"
            v-for="(value, name) in projects"
          >
            <div class="projects-slider-content">
              <h2>{{value.name}}</h2>
              <p>{{value.customer}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

var projects = [
  {
    url: require("../assets/images/stock/project_1.png"),
    name: "Partizipationstool",
    customer: "Landkreis Birkenfeld"
  },
  {
    url: require("../assets/images/stock/project_2.png"),
    name: "Buchungsassistenten",
    customer: "Sparkasse-Rhein Nahe"
  },
  {
    url: require("../assets/images/stock/project_3.png"),
    name: "Filialfinder",
    customer: "Gillen - Der Bäcker"
  },
  {
    url: require("../assets/images/stock/project_4.png"),
    name: "Steuerberater Seite",
    customer: "Steuerberater Daniel Heeb"
  }
];

@Component
export default class Projects extends Vue {
  // @Prop() private msg!: string;
  data() {
    return {
      projects: projects
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#projects-wrapper {
  display: flex;
}

.projects-row {
  display: flex;
}
#projects-headline {
  flex: 1;
}
#projects-items {
  flex: 1;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.projects-item {
  position: relative;
  width: 45%;
  margin-bottom: 2%;
  display: block;
  // flex-direction: column;
  // justify-content: center;

  .projects-image-wrapper {
    width: 100%;
    height: 100%;

    img {
      position: relative;
      width: 100%;
      left: 50%;
      top: 50%;
      // transform: translateX(-50%);
      transform: translate3d(-50%, -50%, 0);

      transition: all 0.5s;
    }
    &:hover {
      img {
        width: 75%;
      }
    }
  }
  .projects-name {
    position: absolute;
    top: 20%;
    left: 0;
    z-index: 20;
    opacity: 0;
    transition: all 0.5s;
  }
  .projects-customer {
    position: absolute;
    bottom: 20%;
    right: 0;
    z-index: 20;
    opacity: 0;
    transition: all 0.5s;
  }
  &:hover {
    .projects-name,
    .projects-customer {
      opacity: 1;
    }
  }
}
.projects-slider-wrapper {
  position: fixed;
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  top: 0;
  .projects-slider {
    top: 50%;
    position: relative;
    transform: translateY(-50%);
    display: flex;
  }
  .projects-slider-items {
    flex-grow: 1;
  }
  .slider-arrows {
    padding: 70px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    img {
      width: 25px;
    }
  }
  .projects-slider-item-wrapper {
    height: 50vh;
    display: none;
    &:first-child {
      display: block;
    }
  }
}
</style>
