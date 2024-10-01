<template>
  <div>
    <b>-------Children Component-------</b>
    <!-- Buoc 3 : lay gia tri ttu props roi render du lieu -->
    <p>Children Company: {{ userNameProps }}</p>
    <p>Child age : {{ ChildAgeProps }}</p>
    <h4>Dữ liệu trong component con</h4>
    <ul>
      <li>ID: {{ infoProductProps.id }}</li>
      <li>Name Product: {{ infoProductProps.name }}</li>
      <li>Price Product: {{ infoProductProps.price }}</li>
      <li>Quantity: {{ infoProductProps.quantity }}</li>
    </ul>
    <button @click="emitIncrement">Increment</button>
  </div>
</template>

<script setup>
// Buoc 1 : Dinh nghia props ben trong component con thong qua phuong thuc
const { userNameProps, ChildAgeProps, infoProductProps } = defineProps([
  "userNameProps",
  "ChildAgeProps",
  "infoProductProps",
]);
const emit = defineEmits(["increment"]);
const emitIncrement = () => {
  emit("increment");
};
console.log(infoProductProps);
</script>

<style></style>
