<template>
  <div>
    <h3>Register {{ name }}</h3>
    <memory-block :name="name" :bytes="bytes"></memory-block>
  </div>
</template>
  
<script setup>
  import MemoryBlock from "./MemoryBlock.vue";
  defineProps({
    name: {
      type: String,
      required: false
    },
    bytes: {
      type: String,
      required: true
    }
  });
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
    border-radius: 5px;
  }

  h3 {
    text-align: center;
  }
</style>