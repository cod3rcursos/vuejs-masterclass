<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<script setup>
import {ref} from "vue"

    const nome = ref("Ana")
    const idade = ref(27)

    function fazerAniversario(){
        idade.value +=1
    }

    function mudarNome(){
        nome.value = "Ana Maria"
    }
</script>