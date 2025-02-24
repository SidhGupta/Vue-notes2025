<template>
  <div>
    <h2>{{ animal.name }}</h2>
    <img :src="animal.image" alt="" />
    <slot></slot>
  </div>
</template>

<script setup>
defineProps({
  animal: Object,
});
</script>

<style scoped></style>
