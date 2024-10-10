<!-- components/SiteTitle.vue -->
<template>
    <h1>{{ text }}</h1>
  </template>

  <script setup>
  defineProps({
    text: {
      type: String,
      required: true
    }
  });
  </script>

  <style scoped>
  h1 {
    font-size: 2rem;
    color: #333;
  }
  </style>