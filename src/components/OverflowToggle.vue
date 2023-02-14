<template>
  <div>
    <div class="label">Overflow</div>
    <div class="overflow-container" v-if="overflow" >
      <div class="overflow-toggle-on overflow-toggle"></div>
    </div>
    <div class="overflow-container" v-else>
      <div class="overflow-toggle-off overflow-toggle"></div>
    </div>
  </div>
</template>

<script setup>
  import { computed } from "vue"
  const overflow = computed({
    get() {
      return false;
    }
  })
</script>

<style scoped>
  .label {
    font-size:14px;
    text-align: center;
  }
  .overflow-toggle-on {
    border: solid 1px red;
    background-color: red;
  }

  .overflow-toggle-off {
    border: solid 1px green;
  }

  .overflow-toggle {
    border-radius: 20px;
    height: 20px;
    width: 20px;
    margin: auto;
    display: flex;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    text-align: center;
  }
  .toggle-container {
    display: inline-block;
    margin: 0px 18px;
  }
</style>