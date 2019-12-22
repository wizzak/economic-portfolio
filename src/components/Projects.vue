<template>
  <div id="projects-wrapper">
    <div id="projects-headline">
      <h2>Projekte</h2>
      <p>Eine Auswahl meiner Projekte an denen ich mitgearbeite habe.</p>
    </div>
    <div id="projects-items">
      <div class="projects-row">
        <div class="projects-item">
          <div class="projects-image-wrapper">
            <img src="../assets/images/stock/project_1.png" alt="project_1" />
          </div>
          <span class="projects-name">Partizipationstool</span>
          <span class="projects-customer">Landkreis Birkenfeld</span>
        </div>
        <div class="projects-item">
          <div class="projects-image-wrapper">
            <img src="../assets/images/stock/project_2.png" alt="project_1" />
            <span class="projects-name">Buchungsassassitent</span>
            <span class="projects-customer">Sparkasse Rhein-Nahe</span>
          </div>
        </div>
      </div>
      <div class="projects-row">
        <div class="projects-item">
          <div class="projects-image-wrapper">
            <img src="../assets/images/stock/project_3.png" alt="project_1" />
          </div>
          <span class="projects-name">Fililafinder</span>
          <span class="projects-customer">Bäckerei Gillen</span>
        </div>
        <div class="projects-item">
          <div class="projects-image-wrapper">
            <img src="../assets/images/stock/project_4.png" alt="project_1" />
          </div>
          <span class="projects-name">Steuerberater Seite</span>
          <span class="projects-customer">Steuerberater Daniel Heeb</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Projects extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#projects-wrapper {
  display: flex;
}
.projects-item {
  flex: 1;
}
.projects-row {
  display: flex;
}
#projects-headline {
  flex: 1;
}
#projects-items {
  flex: 1;
}
.projects-image-wrapper {
  width: 100%;
  img {
    position: relative;
    width: 100%;
  }
}
.projects-item {
  position: relative;
}
.projects-name {
  position: absolute;
}
.projects-customer {
  position: absolute;
}
</style>
