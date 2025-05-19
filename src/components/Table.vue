<script setup>
import { ref, watch } from 'vue';
import tableData from '../common/tableData';

const datas = ref(tableData);
// set는 중복을 허용하지 않아요. array 
const checkedItem = ref(new Set());

// 체크박스 단일 선택
const handleSingleCheck = (checked, id) => {
    if(checked){
        checkedItem.value.add(id);
    } else {
        checkedItem.value.delete(id);
    }
    console.log(checkedItem.value)
}

// 체크박스 전체 선택
const handleAllCheck = (checked) => {
    checkedItem.value = checked ? new Set(datas.value.map(element => element.id)) : new Set();
}

</script>
<template>
    <div>
        <table>
            <thead>
                <tr>
                    <th>
                        <input type="checkbox" @change="handleAllCheck($event.target.checked)" 
                            :checked="checkedItem.size === datas.length"
                       />
                    </th>
                    <th>제목</th>
                    <th>내용</th>
                    <th>만든 날짜</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="data in datas" :key="data.id">
                    <td>
                        <input type="checkbox" @change="handleSingleCheck($event.target.checked, data.id)" 
                            :checked="checkedItem.has(data.id)"
                        />
                    </td>
                    <td>{{ data.title }}</td>
                    <td>{{ data.content }}</td>
                    <td>{{ data.date }}</td>
                </tr>
            </tbody>
        </table>
        {{ checkedItem.size }} 개가 선택 되었습니다.
    </div>
</template>
