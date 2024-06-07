<script setup>
import { ref } from 'vue'
let count = ref(0);
let custom_number = ref(0);

function inc(){
  count.value++;
}

function reset(){
  count.value = this.custom_number;
}
</script>

<template>
  <h1>{{ count }}</h1>
  <button @click="inc()">Increment</button>
  <br>
  <input v-model="custom_number" placeholder="Custom number to reset" value="0"/>
  <button @click="reset()">Reset</button>
</template>
