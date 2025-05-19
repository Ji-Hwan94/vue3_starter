<script setup>
import { ref, watch, watchEffect } from 'vue';

const text = ref("");
const numer = ref(0);

// 값이 변경될 때 두번째 인자의 콜백함수가 실행된다.
// watch(numer, () => {
//     alert(text.value);
// });

watchEffect(() => {
    alert(text.value);
})

</script>

<template>
    <div>
        <input v-model="text"/>
        <br/>
    </div>
</template>