<script setup>
import { ref } from 'vue'

const cont = ref(0)
const words = ref('')

const large = words.value.split(' ')
cont.value = large.length




</script>

<template>

    <div class="w-[400px] h-[300px] mx-auto mt-[200px] bg-slate-200 p-4">
        <div class="inline-block w-[70px] h-[40%] bg-slate-400" ></div>
        <div class="inline-block w-[70px] h-[60%] bg-slate-400 ml-7" ></div>
        <div class="inline-block w-[70px] h-[80%] bg-slate-400 ml-7" ></div>
        <div class="inline-block w-[70px] h-[100%] bg-slate-400 ml-7" ></div>
    </div>
    <div class="flex flex-col items-center my-6 gap-4">
        <input v-model="words" class="border-2 p-3 border-gray-600 rounded-lg w-[250px]" placeholder="Ingrese palabras" type="text">
        <p class="bg-slate-200 px-4 py-2 rounded-2xl font-bold text-lg text-gray-600" >Cont: <span>0</span></p>
    </div>

</template>