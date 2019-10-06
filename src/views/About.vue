<template>
  <div class="about">
    <Resume />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Resume from "@/components/Resume.vue"; // @ is an alias to /src

@Component({
  components: {
    Resume
  }
})
export default class About extends Vue {}
</script>
