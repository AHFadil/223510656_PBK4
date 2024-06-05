<template>
  <div class="grandchild">
    <h3>Grandchild Component</h3>
    <button @click="sendData">Click Me in Grandchild</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue';

const emit = defineEmits(['grandchild-click']);

function sendData() {
  emit('grandchild-click', 'Hello from Grandchild!');
}
</script>

<style scoped>
.grandchild {
  border: 2px solid #e74c3c;
  padding: 20px;
  border-radius: 10px;
  background: linear-gradient(to right, #ff9a9e, #fecfef);
  text-align: center;
}
button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #e74c3c;
  color: white;
  cursor: pointer;
}
button:hover {
  background-color: #c0392b;
}
</style>
