<template>
  <div>
    <h3>Register {{ name }}</h3>
    <table>
      <tr>
        <td>+/-</td>
        <td v-for="k in bytes" :key="k">{{name}}{{k}}</td>
      </tr>
    </table>
  </div>
</template>
  
<script setup>
  import { computed } from "vue"
  const props = defineProps({
    name: {
      type: String,
      required: true
    },
    bytes: {
      type: Number,
      required: true
    }
  });

  const bytes = computed({
    get() {
      return parseInt(props.bytes);
    }
  })

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