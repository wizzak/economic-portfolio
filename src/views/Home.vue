<template>
  <div class="home">
    <section class="hero">
      <HelloWorld />
    </section>
    <section class="project_section">
      <Projects></Projects>
    </section>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src
import Projects from "@/components/Projects.vue";
@Component({
  components: {
    HelloWorld,
    Projects
  }
})
export default class Home extends Vue {}
</script>
