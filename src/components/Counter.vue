<template>
    <div>
      <h2>Visitor Counter</h2>
      <p>Visitors: {{ count }}</p>
      <button @click="count++">Increase Count</button>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const count = ref(0);
      return { count };
    }
  };
  </script>