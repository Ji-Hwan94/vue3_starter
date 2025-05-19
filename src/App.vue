<script setup>
import Button from './components/Button.vue';
import ComputedComponent from './components/ComputedComponent.vue';
import Input from './components/Input.vue';
import ParantComponent from './components/LifeCycle/ParantComponent.vue';
import ManyComponent from './components/ManyComponent.vue';
import SelectBox from './components/SelectBox.vue';
import Table from './components/Table.vue';

</script>

<template>
    <!-- <Button/> -->
    <!-- <Input /> -->
    <!-- <SelectBox /> -->
    <!-- <ManyComponent title="제목1" content="내용1"/>
    <ManyComponent title="제목2" content="내용2"/>
    <ManyComponent title="제목3" content="내용3"/>
    <ManyComponent title="제목4" content="내용4"/>
    <ManyComponent title="제목5" content="내용5"/>
    <ManyComponent title="제목6" content="내용6"/> -->
    <!-- <Table/> -->
    <!-- <ComputedComponent/> -->
    <ParantComponent />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
