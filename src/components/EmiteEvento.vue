<template>
    <div class="componente">
        <h1>Componente que Emite Evento</h1>
        <p>{{ item }} (R${{ preco.toFixed(2) }})</p>
        <button @click="adicionar">Adicionar ao carrinho</button>
    </div>
</template>

<script setup>
import {defineProps, defineEmits} from "vue"

const props = defineProps({
    item:String,
    preco:Number
})

const emit = defineEmits(["foiAdicionado"])

function adicionar(){
    emit("foiAdicionado", props.preco)
}

</script>