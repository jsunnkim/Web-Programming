<template>
  <n-card title="Welcome to My Website">
      <p v-if="showMessage">Hi, This is my website for the Assignment 3</p>
      <n-button @click="showMessage = !showMessage">
      {{ showMessage ? 'Hide' : 'Show' }} Welcome Message
    </n-button>
  </n-card>
</template>

<script setup>
import { ref } from 'vue';
import { NCard, NButton } from 'naive-ui';

const showMessage = ref(true);
</script>