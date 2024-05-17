<script setup>
import { ref } from 'vue';

const arrayList = ref(['Tema 1', 'Tema 2', 'Tema 3', 'Tema 4'])


</script>

<template>

    <section class="">

        <div class="bg-blue-600 w-[500px] m-auto mt-10 p-[6px] flex flex-col">
            <div class="bg-blue-200 py-1 px-4 flex justify-between items-center w-[100%] mb-2 text-blue-900">
                <p class="font-semibold text-lg">Tema 1</p>
                <button class="text-2xl font-bold">+</button>
            </div>
            <div class="bg-blue-100 py-4 px-4 text-blue-900">
                <p class="font-semibold text-sm">Texto del tema 4</p>
            </div>
        </div>

    </section>

</template>