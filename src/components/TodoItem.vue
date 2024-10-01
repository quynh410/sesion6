<template>
  <div>
    <b>-------- TodoItem Component --------</b> <br>
    <button @click="deleteItem">Delete</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue';

const emit = defineEmits(['delete-id']);

function deleteItem() {
  const randomId = Math.floor(Math.random() * 10) + 1;
  emit('delete-id', randomId); 
}
</script>

<style>
</style>
