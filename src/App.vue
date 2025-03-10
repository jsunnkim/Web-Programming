<template>
  <n-layout>
    <!-- Header -->
    <Header :title="'My Assignment 3'" @navigate="handleNavigation" />

    <n-layout-content>
      <component :is="currentComponent"></component>
    </n-layout-content>

    <!-- Footer -->
    <Footer :message="'Thanks for visiting!'" />
  </n-layout>
</template>

<script>
import { ref, computed } from 'vue';
import { NLayout, NLayoutContent } from 'naive-ui';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Home from './components/Home.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

export default {
  components: { Header, Footer, NLayout, NLayoutContent },
  setup() {
    const currentSection = ref('home');

    const currentComponent = computed(() => {
      return currentSection.value === 'home' ? Home :
             currentSection.value === 'projects' ? Projects :
             Contact;
    });

    const handleNavigation = (section) => {
      currentSection.value = section;
    };

    return { currentSection, currentComponent, handleNavigation };
  }
};
</script>