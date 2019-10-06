<template>
  <div class="resume-wrapper">
    <div class="resume-col-wrapper">
      <div id="resume-col-1" class="resume-col">
        <div class="resume-col-heading">
          <h2>Basic</h2>
        </div>
        <div class="resume-col-content">
          <ul>
            <li>1 station</li>
            <li>2 station</li>
            <li>3 station</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="resume-col-wrapper">
      <div id="resume-col-2" class="resume-col">
        <div class="resume-col-heading">
          <h2>Standard</h2>
        </div>
        <div class="resume-col-content">
          <ul>
            <li>1 station</li>
            <li>2 station</li>
            <li>3 station</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="resume-col-wrapper">
      <div id="resume-col-3" class="resume-col">
        <div class="resume-col-heading">
          <h2>Premium</h2>
        </div>
        <div class="resume-col-content">
          <ul>
            <li>1 station</li>
            <li>2 station</li>
            <li>3 stationd</li>
            <li>4 stationd</li>
            <li>5 stationd</li>
          </ul>
        </div>
      </div>
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
.resume-wrapper {
  display: flex;
  justify-content: space-around;
  .resume-col-wrapper {
    margin: 0 15px;
  }
  .resume-col {
    border: 1px solid;
    overflow: hidden;
    height: 100%;
    // padding: 0 5rem 4rem;
    border-radius: 10px;
    background-color: #ffffff47;
    .resume-col-heading {
      text-align: center;
      background-color: white;
      color: black;
      padding: 1rem 5rem;

      h2 {
        margin: 0;
      }
    }
  }
  #resume-col-3 {
    box-shadow: -6px 6px 8px rgba(255, 255, 255, 0.2);
  }
}
</style>
