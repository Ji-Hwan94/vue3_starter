<script setup>
import { computed, ref } from 'vue';

// 시간이 오래 걸리는 함수
const generateData = () => {
    return Array.from({ length:10000 }, ( _, i ) => ({
        id: i + 1,
        name: `Item ${i+1}`,
        values: Math.floor(Math.random() * 1000)
    }))
}

const data = generateData();

const search = ref("");

const filteredDataCount = () => {
    console.log("검색 결과가 나왔어요");
    return data.filter((item) => 
        item.name.toLowerCase().includes(search.value.toLowerCase())
    ).length;
};

const filteredDataCountComputed = computed(
    () => {
    console.log("Computed을 사용한 검색 결과가 나왔어요");
    return data.filter((item) => 
        item.name.toLowerCase().includes(search.value.toLowerCase())
    ).length;
}
)
</script>
<template>
    <div>
        <input v-model="search"/>
        <p>검색 결과 개수: {{ filteredDataCountComputed }}</p>
        <br />
        <p>{{ filteredDataCountComputed }} 개의 검색 결과로 무엇을 할 것인가요?</p>
    </div>
</template>
