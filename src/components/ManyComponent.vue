<script setup>
const { title, content } = defineProps(["title", "content"]);
</script>
<template>
    <div>
        <h2>{{ title }}</h2>
        <p>{{ content }}</p>
    </div>
</template>
