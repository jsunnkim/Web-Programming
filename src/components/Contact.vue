<template>
  <n-card title="Contact Me">
    <form @submit.prevent="handleSubmit">
      <n-input v-model="name" placeholder="Your Name" />
      <n-input v-model="email" placeholder="Your Email" type="email" />
      <n-input type="textarea" v-model="message" placeholder="Your Message" />
      <n-button type="primary" @click="handleSubmit">Send</n-button>
    </form>
  </n-card>
</template>

<script setup>
import { ref, watch } from 'vue';
import { NCard, NInput, NButton } from 'naive-ui';

const name = ref('');
const email = ref('');
const message = ref('');

watch([name, email, message], () => {
  console.log(`Form updated: ${name.value}, ${email.value}, ${message.value}`);
});

const handleSubmit = () => {
  alert(`Message Sent! Name: ${name.value}, Email: ${email.value}`);
  name.value = '';
  email.value = '';
  message.value = '';
};
</script>