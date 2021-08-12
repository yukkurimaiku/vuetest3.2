<template>
  <div>
    <button @click="color = color === 'red' ? 'green' : 'red'">
      Color is: {{ color }}
    </button>
    <kodomo :color="color" @action="action" />
    <div class="text">aa</div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue';
import Kodomo from './components/Kodomo.vue';

const color = ref('red');
const colors = reactive({
  text: 'blue',
});

function action(msg) {
  console.log(msg);
}
</script>

<style scoped>
button {
  color: v-bind(color);
}
.text {
  color: v-bind('colors.text');
}
</style>
