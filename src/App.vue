<script setup>
// import BaseButton from "./components/BaseButton.vue";
import ParentComponenet from "./components/ParentComponenet.vue";
import TodoList from "./components/TodoList.vue";
// import SlotComponent from "./components/SlotComponent.vue";

// const handleClick = () => {
//   console.log("Click button");
// };
// const handleClickParent = (data)=>{
//   console.log("du lieu truyen tu con len : ",data);

// }

import Modal from "./components/Modal.vue";
import { ref } from "vue";
const isModalVisible = ref(false);

const showModal = () => {
  isModalVisible.value = true;
};

const closeModal = () => {
  isModalVisible.value = false;
};
const viewDetails = () => {
  alert("Xem chi tiết sản phẩm!");
};
</script>

<template>
  <div>
    <parent-componenet> </parent-componenet>
    <p>_______________________________________________</p>
    <slot-component>
      <!-- Noi dung nay se chinh la slot sau nay dung -->
      <a href="">facebook</a>
    </slot-component>
    <hr />
    <base-button @onClick="handleClickParent">
      <!-- Noi dung nay se chinh la slot duoi nay dung -->

      <div>Click me</div>
    </base-button>
    <TodoList></TodoList>
    <modal></modal>

    <button @click="showModal">Open Modal</button>
    <Modal
      v-if="isModalVisible"
      :title="'Thông báo từ hệ thống'"
      :isVisible="isModalVisible"
      @close="closeModal"
    >
      Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút
      'Close'.
    </Modal>

    
    <button @click="showModal">Open</button>
    <Card>
      <!-- Header -->
      <template> Thông tin sản phẩm </template>
      <!-- Body -->
      <template>
        Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật
        và giá cả hợp lý.
      </template>
      <!-- Footer -->
      <template>
        <button @click="viewDetails">Xem chi tiết</button>
      </template>
    </Card>
  </div>
</template>

<style>
button {
  border: 1px solid black;
  width: 100px;
  height: 40px;
  border-radius: 5px;
  background: white;
}
</style>
