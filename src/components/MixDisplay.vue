<template>
    <v-container class="bg-surface-variant">
    <v-row no-gutters>
      <v-col
        v-for="n in ['A','B', 'C']"
        :key="n"
        cols="4"
      >
          <span>Register {{n}}</span>
         
      </v-col>
    </v-row>
 </v-container>
</template>

<script setup>
</script>

<style scoped>
  .show-border {
    border: 1px solid white;
  }

  .register-box {
    width: 50px;
    height: 50px;
  }
</style>