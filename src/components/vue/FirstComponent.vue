<script setup>
import { ref } from "vue"

let number = ref(5);

function add() {
    number.value++
    console.log(number)
}
function rest() {
    if (number.value > 0) {

        number.value--
    }

}

</script>

<template class="h-svh">
    <div class="max-w-96  bg-blue-700 rounded-xl  py-5 px-9 mx-auto">
        <div class="bg-red-400 size-8 flex items-center mx-auto justify-center rounded-full" v-if="number > 0">
            {{ number }}
        </div>
        <div v-else class="bg-white rounded-lg w-max m-auto p-2">
            🥲 nadie te escribe 🥲
        </div>

        <div class=" flex justify-center space-x-5 py-3">
            <div class="bg-purple-400 size-8 flex items-center cursor-pointer  justify-center rounded-full"
                @click="add()">
                +
            </div>
            <div class="bg-purple-400 size-8 flex items-center cursor-pointer justify-center rounded-full"
                @click="rest()">
                -
            </div>
        </div>

    </div>
</template>