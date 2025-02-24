<script setup>
import { ref, computed } from "vue";

const searchQuery = ref("");
const users = ref([
  { id: 1, name: "Alice" },
  { id: 2, name: "Bob" },
  { id: 3, name: "Charlie" },
  { id: 4, name: "David" },
]);

const filteredUsers = computed(() =>
  users.value.filter((user) =>
    user.name.toLowerCase().includes(searchQuery.value.toLowerCase())
  )
);
</script>

<template>
  <div>
    <input v-model="searchQuery" placeholder="Search users..." />
    <ul>
      <li v-for="user in filteredUsers" :key="user.id">
        {{ user.name }}
      </li>
    </ul>
  </div>
</template>
