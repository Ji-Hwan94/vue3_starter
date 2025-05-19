<script setup>
import { ref } from 'vue';

const selectedValue = ref("2");

</script>
<template>
    <div>
        <select v-model="selectedValue">
            <option value="1">1번</option>
            <option value="2">2번</option>
            <option value="3">3번</option>
            <option value="4">4번</option>
        </select>
        선택된 값 : {{ selectedValue }}
    </div>
</template>
