<script setup>
import { ref } from 'vue';

const cont = ref(0)
const arrayList = [{tittle:'Tema 1',context:'Texto del tema 1'},{tittle:'Tema 2',context:'Texto del tema 2'},{tittle:'Tema 3',context:'Texto del tema 3'},{tittle:'Tema 4',context:'Texto del tema 4'}]

function selectCage(index) {
    
    if (index == cont.value) {
        cont.value = -1
    }else {
        cont.value = index
    }

}

</script>

<template>

    <section class="bg-blue-600 w-[500px] m-auto mt-10 p-[7px] flex flex-col">

        <div v-for="(arrList, index) in arrayList" :key="index">
            <button @click="selectCage(index)" class="bg-blue-200 py-1 px-4 flex justify-between items-center w-[100%] mb-1 text-blue-900"
                :class="{'bg-blue-900 text-white': cont == index}">
                <p class="font-semibold text-lg">{{ arrList.tittle }}</p>
                <p v-if="cont !== index" class="text-2xl font-bold">+</p>
                <p v-else class="text-2xl font-bold">-</p>
            </button>
            <div v-show="cont == index" class="bg-blue-100 py-4 px-4 text-blue-900 mb-2">
                <p class="font-semibold text-sm">{{ arrList.context }}</p>
            </div>
        </div>

    </section>

</template>