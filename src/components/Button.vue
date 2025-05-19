<script setup>
import { ref } from 'vue';
// state 값 생성하는 법
const count = ref(0);

const increment = () => {
    count.value++;
}
</script>

<template>
    <div>
        <!-- 버튼을 클릭하게 되면 count라는 값이 증가가 될 겁니다.-->
        <button @click="increment">
            <!-- 값을 브라우저에 넘기는 법 -->
            conut is {{ count }}
        </button>
    </div>
</template>
