<template>
  <div class="parent">
    <h1>Parent Component</h1>
    <p>{{ message }}</p>
    <ChildComponent @child-click="handleChildClick" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

const message = ref('');

function handleChildClick(data) {
  message.value = data;
}
</script>

<style scoped>
.parent {
  border: 2px solid #42b983;
  padding: 20px;
  border-radius: 10px;
  background: linear-gradient(to right, #ffecd2, #fcb69f);
  text-align: center;
}
</style>
