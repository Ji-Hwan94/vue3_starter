<script setup>
import { ref, watch } from 'vue';
import ChildComponent from './ChildComponent.vue';

const hide = ref(false);

</script>
<template>
    <div>
        <h2>ParantComponent</h2>
        <button @click="hide = !hide">자식 컴포넌트 등장 해주세요</button>
        <br/>
        <ChildComponent v-if="hide"/>
    </div>
</template>