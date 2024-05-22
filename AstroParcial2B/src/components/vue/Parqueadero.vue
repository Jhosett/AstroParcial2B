<script setup>
import { ref } from 'vue';

const arrMotos = ref([true,true,false,true,true,false,true,true,true]);
const arrCarros = ref([true,true,false,true,true,false,true,true,true,false,true,true]);

const counter = ref(0)

function changeColor(i, array, precio) {
    if (!array[i]) {
        counter.value += precio
    }

    array[i] = !array[i]
}


</script>

<template>
    <p class="font-bold text-3xl my-4 text-center">Total: ${{ counter }}</p>
    <div class="flex justify-between mx-[590px] font-semibold text-2xl mt-16">
        <p>Parqueadero Motos</p>
        <p>Parqueadero Carros</p>
    </div>
    <div class="flex justify-center gap-10 p-10">
        <section class="w-[400px] grid grid-cols-3 gap-5">
            <div @click="changeColor(i, arrMotos, 1000)" v-for="(array, i) in arrMotos" class="w-full h-28"
            :class="{'bg-green-600' :array}, {'bg-red-500' :!array}"></div>
        </section>

        <section class="w-[600px] grid grid-cols-4 gap-5">
            <div @click="changeColor(i, arrCarros, 2000)" v-for="(array, i) in arrCarros" class="w-full h-28"
            :class="{'bg-green-600' :array}, {'bg-red-500' :!array}"></div>
        </section>
    </div>

</template>