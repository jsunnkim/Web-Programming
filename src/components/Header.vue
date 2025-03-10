<template>
  <n-layout-header bordered>
    <n-space justify="space-between" align="center">
      <h1>{{ title }}</h1>
      <n-space>
        <n-button @click="$emit('navigate', 'home')">Home</n-button>
        <n-button @click="$emit('navigate', 'projects')">Projects</n-button>
        <n-button @click="$emit('navigate', 'contact')">Contact</n-button>
      </n-space>
    </n-space>
  </n-layout-header>
</template>

<script setup>
import { NLayoutHeader, NSpace, NButton } from 'naive-ui';

defineProps({
  title: String,
});

defineEmits(['navigate']);
</script>

<style scoped>
h1 {
  font-size: 24px;
  margin-left: 15px;
}
</style>