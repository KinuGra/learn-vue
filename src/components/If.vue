<script setup>
import { ref } from 'vue';

    const error = "";
    let flag = ref(0);
    const callback = () => {
        if (flag.value > 1) {
            flag.value = 0;
        } else {
            flag.value++;
        }
    };
    setInterval(callback, 2000)

    // callback これは関数が参照渡しされる
    // callback() これは実行結果の返り値、undefindが渡される
</script>

<template>
    <!-- v-ifディレクティブ -->
    <div v-if="error">{{ error }}</div>
    <div v-else>エラーはありません</div>

    <div v-if="flag.value === 0">flag == {{ flag.value }}</div>
    <div v-else-if="flag.value === 1">flag == {{ flag }}</div>
    <div v-else>flag == {{ flag }}</div>

    <div v-if="false">
        <div>
            <h1>aiueo</h1>
        </div>
    </div>

    <!-- falseの時v-showの場合は要素が存在し、style属性でdisplay:noneが設定される -->
    <div v-show="flag === 0">flag が0であることをv-showで表示</div>
</template>