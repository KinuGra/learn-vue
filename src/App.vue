<script setup>
console.log("Hello, World")
let message = "Hello World"
const htmlMesssage = "<h2>Hello H2 World";
const array = [1,2,3,4,5]

const upperCase = () => {
  message = message.toUpperCase();
};
upperCase();
</script>

<template>
<h1>Vue 3 入門</h1>

<p>{{ message }}</p>
<p v-text="htmlMesssage"></p>
<div v-html="htmlMesssage"></div>

<!-- マスタッシュ -->
<div>{{ message.length * 10 }}</div>
<p>{{ array.map((e) => e*2) }} </p>
<div>{{ array[0] == 1 ? 'true' : 'false' }}</div>
</template>