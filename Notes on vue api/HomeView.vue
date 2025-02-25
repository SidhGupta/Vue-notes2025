<template>
    <div>
        <div>

        </div>
    </div>
</template>



<script>
import {ref, onMounted} from "vue";
const pokemon = ref("");
async function getPokemon() {
    let res = await fetch("")
    let data = await res.json();
    pokemon.value = data.results;
}






</script>