<template>
  <!-- Buoc 2 : phat di 1 cai su kien thong qua emit  -->
  <button @click="handleClick">
    <slot></slot>
  </button>
</template>

<script setup>
const props = defineProps({
  title: {
    default: "Click me ",
    type: String,
    required: true,
  },
});
// Buoc 1 : khoir tao cac emit
const emit = defineEmits(["onClick"]);
const handleClick = () => {
  // emit ra su kien onClick
  emit("onClick", "Xin chao cac ban");
};
</script>

<style></style>
