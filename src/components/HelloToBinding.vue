<script setup>
console.log("Hello, World")
let message = "Hello World"
const htmlMesssage = "<h2>Hello H2 World";
const array = [1,2,3,4,5]

const link = 'https://google.com'
const path = '/vite.svg'
const isActive = false, isBlack = true;

const activeColor = 'red';
const fontStress = '900';
const styleObject = {
  color: 'blue',
  fontWeight: 900,
};

const upperCase = () => {
  message = message.toUpperCase();
};
upperCase();
</script>

<template>
<h1>Vue 3 入門</h1>

<!-- v-bindの設定 -->
<p class="active">v-bindの設定方法の確認</p>
<p class="underLine" :class="{ active: isActive }">v-bindの設定方法の確認</p>
<p :class="{ 'underLine active': !isActive, back: isBlack }">v-bindの設定方法の確認</p>
<p :class="{ active: !isActive, back: isBlack }">v-bindの設定方法の確認</p>
<p :style="{ color: activeColor, 'font-weight': fontStress }">v-bindの設定方法の確認(style)</p>
<p :style="styleObject">v-bind (styleObject)</p>

<p>{{ message }}</p>
<p v-text="htmlMesssage"></p>
<div v-html="htmlMesssage"></div>

<!-- マスタッシュ -->
<div>{{ message.length * 10 }}</div>
<p>{{ array.map((e) => e*2) }} </p>
<div>{{ array[0] == 1 ? 'true' : 'false' }}</div>

<!-- Binding -->
<a v-bind:href="link">Google</a>
<img :src="path">
</template>

<style>
.active {
  color: red;
  font-weight: 900;
}
.underLine {
  text-decoration: underline;
}
.back {
  background-color: black;
}
</style>