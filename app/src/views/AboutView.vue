<template>
  <div>
    <NewList />
    <form name="login-form" @submit.prevent="login(user)">
      <label for="username">Enter Username</label>
      <input type="text" v-model="user.username" />
      <label for="password">Enter Password</label>
      <input type="text" v-model="user.password" />
      <button class="submit-button" type="submit">Login</button>
    </form>
    <h2 v-if="skibidi">Mark Fridlan</h2>
    <h2 v-else>Mark Fridl-Fam</h2>
  </div>
</template>

<script setup>
import NewList from '../components/NewList.vue'
import { reactive } from 'vue'
const user = reactive({ username: '', password: '' })
function login(user) {
  console.log(user)
}
const skibidi = false
</script>

<style scoped></style>
