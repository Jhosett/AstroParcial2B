<script setup>
import { ref } from 'vue'

var cont = ref(0)
var words = ref('')

function build() {
    var large = words.value.split(' ')
    cont.value = large.length
}

function showColor1() {
    if (cont.value>0 && cont.value>=2) {
        return true
    }
}

function showColor2() {
    if (cont.value>2 && cont.value>=4) {
        return true
    }
}

function showColor3() {
    if (cont.value>4 && cont.value>=6) {
        return true
    }
}

function showColor4() {
    if (cont.value>6) {
        return true
    }
}


//  function recorrido() {
//     for (let index = 0; index < large.length; index++) {
//         cont ++
//     }
//  }

</script>

<template>

    <div class="w-[400px] h-[300px] mx-auto mt-[200px] bg-slate-200 p-4">
        <div 
        class="inline-block w-[70px] h-[40%] bg-slate-400"
        :class="{'bg-red-500': cont>0 && cont>=2}"
        ></div>
        <div 
        class="inline-block w-[70px] h-[60%] bg-slate-400 ml-7" 
        :class="{'bg-orange-500': cont>2 && cont>=4}"
        ></div>
        <div 
        class="inline-block w-[70px] h-[80%] bg-slate-400 ml-7" 
        :class="{'bg-yellow-500': cont>4 && cont>=6}"
        ></div>
        <div 
        class="inline-block w-[70px] h-[100%] bg-slate-400 ml-7" 
        :class="{'bg-green-500': cont>6}"
        ></div>
    </div>
    <div class="flex flex-col items-center my-6 gap-4">
        <input v-model="words" class="border-2 p-3 border-gray-600 rounded-lg w-[250px]" placeholder="Ingrese palabras" type="text">
        <!-- <p class="bg-slate-200 px-4 py-2 rounded-2xl font-bold text-lg text-gray-600" >Cont: <span>{{ cont }}</span></p> -->
    </div>

</template>