<template>
  <div>
    <div class="label">Comparison</div>
    <div>
      <span class="toggle-container" v-if="less" >
        <div class="overflow-toggle-on overflow-toggle">L</div>
      </span>
      <span class="toggle-container" v-else>
        <div class="overflow-toggle-off overflow-toggle">L</div>
      </span>
      <span class="toggle-container" v-if="equal" >
        <div class="overflow-toggle-on overflow-toggle">E</div>
      </span>
      <span class="toggle-container" v-else>
        <div class="overflow-toggle-off overflow-toggle">E</div>
      </span>
      <span class="toggle-container" v-if="greater" >
        <div class="overflow-toggle-on overflow-toggle">G</div>
      </span>
      <span class="toggle-container" v-else>
        <div class="overflow-toggle-off overflow-toggle">G</div>
      </span>
    </div>
  </div>
</template>

<script setup>
  import { computed } from "vue"
  const less = computed({
    get() {
      return false;
    }
  })
  const equal = computed({
    get() {
      return false;
    }
  })
  const greater = computed({
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