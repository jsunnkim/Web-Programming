<template>
  <n-card title="My Projects">
    <p v-if="projects.length === 0">No projects available</p>
    <ul>
      <li v-for="(project, index) in projects" :key="index">
        {{ project.name }}
      </li>
    </ul>
    <p>Total Projects: {{ projectCount }}</p>
  </n-card>
</template>

<script setup>
import { ref, computed } from 'vue';
import { NCard } from 'naive-ui';

const projects = ref([
  { name: "1" },
  { name: "2" },
  { name: "3" }
]);

const projectCount = computed(() => projects.value.length);
</script>