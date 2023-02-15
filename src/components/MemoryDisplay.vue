<template>
    <div class="display-container">
      <!-- <v-card class="display">
        <div v-for="n in 4000" :key="n">
          <v-container>
            <v-row>
              <v-col>
                {{ memNum(n) }}
              </v-col>
              <v-col>
                  <MemoryBlock bytes="5"></MemoryBlock>
              </v-col>
            </v-row>
          </v-container>
        </div>
      </v-card> -->
      <v-card class="display">
        <div v-for="n in 4000" :key="n">
          <span class="memory-slot memory-span">{{ memNum(n - 1) }}</span>
          <span class="memory-span"><MemoryBlock bytes="5"></MemoryBlock></span>
        </div>
      </v-card>
    </div>
  </template>
  
  <script setup>
    import MemoryBlock from './MemoryBlock.vue';
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
  </style>