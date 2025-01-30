<script setup>
import LogIn from "../components/LogIn.vue";
import AnimalCard from "../components/AnimalCard.vue";
const animals = [
  { name: "Capybara", image: "/capy.jpg" },
  { name: "Walrus", image: "/walrus.webp" },
];
</script>

<template>
  <main>
    <LogIn message="Hello World" :count="5"><h1>Hello Laith</h1></LogIn>
    <AnimalCard v-for="animal in animals" :key="animal.name" :animal="animal" />
  </main>
</template>
