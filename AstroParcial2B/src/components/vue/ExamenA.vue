<script setup>
import { ref } from "vue";
import HomeIcon from "./HomeIcon.vue"
import ArrowRightIcon from "./ArrowRightIcon.vue"
import ArrowDownIcon from "./ArrowDownIcon.vue";
import CarpetIcon from "./CarpetIcon.vue"
import { estructure } from "../constants";

const cajaPrincipal = ref(estructure)
let show = ref(false)

function mostrar() {
    if (show.value == false) {
        show.value = true
    } else {
        show.value = false
    }
}

function mostrarSubCarpeta(arrFiles, index) {
    if (arrFiles.status == false) {
        arrFiles.status = true
    } else {
        arrFiles.status = false
    }
    console.log(arrFiles);
}

</script>

<template>
    <section>
        <div class="mx-auto p-4 my-[20%] w-[400px] bg-gray-200" >

            <div @click="mostrar()"
            class="flex items-center gap-2 select-none hover:cursor-pointer hover:font-bold" 
            >
                <HomeIcon/>
                <p>Home</p>
                <ArrowRightIcon v-if="show == false"/>
                <ArrowDownIcon v-else/>
            </div>

            <div @click="mostrarSubCarpeta(arrFiles, index)"
            v-show="show == true"
            v-for="(arrFiles, index) in cajaPrincipal"
            class="flex items-center my-4 ml-5 hover:cursor-pointer hover:font-bold select-none" 
            >
                <CarpetIcon class="mr-3" />
                {{ arrFiles.name }}
                <ArrowRightIcon v-if="arrFiles.status == false"/>
                <ArrowDownIcon v-else/>
            </div>

        </div>
    </section>
</template>