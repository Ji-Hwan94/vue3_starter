<script setup>
import { onBeforeMount, onMounted, onUnmounted, onUpdated, ref, watch, watchEffect } from 'vue';

const count = ref(0);
onMounted(() => {
    alert("onMounted");
});

onUnmounted(() => {
    alert("onUnmounted");
});

onUpdated(() => {
    alert("onUpdated")
});
</script>
<template>
    <div class="card">
        <h3>ChildComponent</h3>
        <p>카운트 : {{ count }}</p>
        <button @click="count++">증가</button>
    </div>
</template>
<style scoped>
.card {
    border: 1px solid #000;
}
</style>