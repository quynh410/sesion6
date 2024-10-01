<template>
  <div>
    <b>-------- TodoApp Component --------</b>
    <p>Id to delete: {{ idToDelete }}</p>
    <TodoItem @delete-id="handleDeleteId" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import TodoItem from './TodoItem.vue';

const idToDelete = ref(null);

const handleDeleteId=(id)=> {
  idToDelete.value = id;
}
</script>

<style></style>
