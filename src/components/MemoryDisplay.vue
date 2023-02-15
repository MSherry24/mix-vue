<template>
    <div class="display-container">
      <v-card class="display">
        <table class="mem-table">
          <tbody>
            <tr v-for="n in 4000" :key="n">
              <td>{{ memNum(n-1) }}</td>
              <td class="mem-block">+/-</td>
              <td class="mem-block"></td>
              <td class="mem-block"></td>
              <td class="mem-block"></td>
              <td class="mem-block"></td>
              <td class="mem-block"></td>
            </tr>
          </tbody>
        </table>
      </v-card>
    </div>
  </template>
  
  <script setup>
    const memNum = (n) => {
      let stringN = n.toString();
      while (stringN.length < 4) {
        stringN = '0' + stringN;
      }
      return stringN;
    }
  </script>
  
  <style scoped>
   .memory-span {
      display: inline-block;
   }
   .display-container {
      width: 400px;
      max-height: 300px;
      overflow-y: scroll;
   }

   .memory-slot {
    text-align: right;
    display: flex;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    text-align: center;
   }

   .mem-block {
    border: solid 1px black;
    width: 40px;
    height: 40px;
    border-radius: 5px;
    text-align: center;
   }

   .mem-table {
    margin: auto;
   }
  </style>