<template>子供</template>

<script setup>
import { defineProps, onMounted } from 'vue';

const props = defineProps({
  color: {
    type: String,
    default: '',
  },
});

const emit = defineEmits(['action']);

onMounted(() => {
  console.log(props.color);
  emit('action', '野郎');
});
</script>

<style></style>
