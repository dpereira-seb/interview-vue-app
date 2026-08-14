<script setup>
// Front-end coding test
// 1. Implement a reusable <VSelect> component.
//    Clicking an item selects it and updates v-model.
// 2. Use v-model for two-way binding.
// 3. Always show the dropdown menu (no toggle for now).
// 4. Use TypeScript

import { ref } from 'vue';

const countryCode = ref();
const countries = [
  { code: "fr", name: "France" },
  { code: "de", name: "Germany" },
  { code: "in", name: "India" },
  { code: "it", name: "Italy" },
  { code: "jp", name: "Japan" },
  { code: "us", name: "United States" },
  { code: "uk", name: "United Kingdom" },
  { code: "ca", name: "Canada" },
  { code: "au", name: "Australia" },
];
</script>

<template>
  <h1>Front-end coding test</h1>
  <div>
    <VSelect v-model="countryCode" :items="countries" />
    <p>Selected: {{ countryCode }}</p>
  </div>
</template>
