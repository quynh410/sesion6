<template>
  <div>
    <slot></slot>
    <b>-------Parent Component-------</b>
    <p>Parent Company : {{ userName }}</p>
    <p>Count : {{count}}</p>
    <p>_______________________________________________</p>
    <children-component
      :userNameProps="userName"
      :ChildAgeProps="age"
      :infoProductProps="infoProduct"
      @increment="incrementCount"
    ></children-component>
    <!-- Su dung component con  -->
    <!-- Buoc 2 trong components cha , goi prop dc khai bao ben con va truyen gia tri cho no -->
  </div>
</template>

<script setup>
import { ref } from "vue";
import ChildrenComponent from "./ChildrenComponent.vue";
const userName = "Rikkei Academy";
const count = ref(0)
// tao bien tuoi truyen tu parent xuong con
const age = 19;
const infoProduct = {
  id: 1,
  productName: "Bưởi Ba Roi",
  price: "12.000đ",
  quantity:10
};
const incrementCount = () => {
  count.value++;
};
</script>

<style></style>
