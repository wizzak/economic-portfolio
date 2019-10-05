<template>
  <div class="hello">
    <div class="name">
      <span>Christoph Weis</span>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.name {
  display: flex;
  align-items: center;
  span {
    font-size: 46px;
    letter-spacing: 10px;
  }
}
.hello {
  height: 95vh;
  width: 100%;
  display: flex;
}
</style>
