<template>
  <div class="card">
    <div class="card-header">
      <slot name="header"></slot>
    </div>
    <div class="card-body">
      <slot name="body"></slot>
    </div>
    <div class="card-footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  width: 300px;
  margin: 20px auto;
}

.card-header {
  font-weight: bold;
  margin-bottom: 10px;
}

.card-body {
  margin-bottom: 20px;
}

.card-footer button {
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card-footer button:hover {
  background-color: #0056b3;
}
</style>
