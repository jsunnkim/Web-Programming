<template>
  <n-layout-footer bordered>
    <p>{{ message }}</p>
  </n-layout-footer>
</template>

<script setup>
import { NLayoutFooter } from 'naive-ui';

defineProps({
  message: String,
});
</script>

<style scoped>
p {
  text-align: center;
  padding: 10px;
}
</style>