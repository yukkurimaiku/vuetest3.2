<template>
  <div>
    <button @click="color = color === 'red' ? 'green' : 'red'">
      Color is: {{ color }}
    </button>
    <kodomo :color="color" @action="action" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Kodomo from './components/Kodomo.vue';

const color = ref('red');

function action(msg) {
  console.log(msg);
}
</script>

<style scoped>
button {
  color: v-bind(color);
}
</style>
