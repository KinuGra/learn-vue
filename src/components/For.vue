<script setup>
const languages = ['Rust', 'React', 'Vue.js'];
const users = [
  { id: 1, name: 'John Doe', email: 'john@test.com', admin: true },
  { id: 2, name: 'Jane Doe', email: 'jane@example.com', admin: false },
  { id: 3, name: 'Kevin MacDonald', email: 'kevin@test.com', admin: false },
];
</script>

<template>
    <p v-for="language in languages" :key="language">{{ language }}</p>
    <span v-for="user in users" :key="user">{{ user }}<br></br></span>
    <div v-for="(user, i) in users" :key="user.id">{{ i }}:{{ user.name }}</div>
</template>