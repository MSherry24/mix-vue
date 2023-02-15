<template>
  <v-container class="">
    <v-row>
      <v-col>
        <mix-register name="A" bytes="5"></mix-register>
      </v-col>
      <v-col>
        <mix-register name="X" bytes="5"></mix-register>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3">
        <div><mix-register name="I1" bytes="2"></mix-register></div>
        <div><mix-register name="I2" bytes="2"></mix-register></div>
        <div><mix-register name="I3" bytes="2"></mix-register></div>
        <div><mix-register name="I4" bytes="2"></mix-register></div>
        <div><mix-register name="I5" bytes="2"></mix-register></div>
      </v-col>
      <v-col cols="9">
        <div>
          <v-container>
            <v-row>
              <v-col>
                <overflow-toggle></overflow-toggle>
              </v-col>
              <v-col>
                <comparison-toggle></comparison-toggle>
              </v-col>
            </v-row>
          </v-container>
        </div>
        <div class="display-container">
          <memory-display></memory-display>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
  import MixRegister from './MixRegister.vue';
  import OverflowToggle from './OverflowToggle.vue';
  import ComparisonToggle from './ComparisonToggle.vue';
  import MemoryDisplay from './MemoryDisplay.vue';
</script>
<script>
  export default {
    data: () => ({
      alignments: [
        'start',
        'center',
        'end',
      ],
    }),
  }
</script>

<style scoped>
  .show-border {
    border: 1px solid white;
  }

  td {
    border: solid 1px black;
    text-align: center;
    width: 40px;
    height: 40px;
  }

  h3 {
    text-align: center;
  }
  .split {
    height: 100%;
    width: 50%;
    position: fixed;
    z-index: 1;
    top: 0;
    overflow-x: hidden;
    padding-top: 20px;
  }
  .left {
    left: 0;
  }

  .right {
    right: 0;
  }

  .display-container {
    position: absolute;
  }

  .display {
    text-align: center;
    position: relateive;
    height: 100%;
    width: 100%;
  }
</style>