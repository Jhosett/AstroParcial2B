<script setup>
import { ref } from 'vue';
import CheckedIcon from './CheckedIcon.vue'



</script>

<template>

    <div class="bg-slate-200 max-w-[500px] mx-auto mt-10 p-3">
        <div class="w-full bg-white p-1" >
            <p class="text-end text-xs font-semibold text-gray-400 h-0" >Marcar como leído</p>
            <div class="flex items-center m-1" >
                <CheckedIcon class="ml-2 mr-4 text-green-500 text-xl" />
                <div>
                    <p class="font-bold text-base" >Correo 1</p>
                    <p class="font-semibold text-sm text-gray-700">Texto del correo 1</p>
                    <p class="text-xs text-gray-400" >Hace una hora</p>
                </div>
            </div>
        </div>
    </div>

</template>