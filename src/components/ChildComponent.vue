<template>
  <div class="child">
    <h2>Child Component</h2>
    <button @click="sendDataFromChild">Click Me in Child</button>
    <GrandChildComponent @grandchild-click="handleGrandchildClick" />
  </div>
</template>

<script setup>
import GrandChildComponent from './GrandChildComponent.vue';
import { defineEmits } from 'vue';

const emit = defineEmits(['child-click']);

function handleGrandchildClick(data) {
  emit('child-click', data);
}

function sendDataFromChild() {
  emit('child-click', 'Hello from Child!');
}
</script>

<style scoped>
.child {
  border: 2px solid #35495e;
  padding: 20px;
  border-radius: 10px;
  background: linear-gradient(to right, #a1c4fd, #c2e9fb);
  text-align: center;
}
button {
  margin-bottom: 20px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #35495e;
  color: white;
  cursor: pointer;
}
button:hover {
  background-color: #2c3e50;
}
</style>
