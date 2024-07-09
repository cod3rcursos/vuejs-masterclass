<template>
	<div class="componente">
		<h1>Componente Com Dados Reativos Primitivos</h1>
		<p>Nome: {{ nome }} | Idade: {{ idade }}</p>
		<button v-on:click="fazerAniversario">Fazer Aniversário</button>
		<button @click="mudarNome()">Mudar Nome</button>
	</div>
</template>

<script>
import { ref } from "vue";
export default {
	setup: function () {
		const nome = ref("Ana");
		const idade = ref(27);

		function fazerAniversario() {
			idade.value += 1;
		}

		function mudarNome() {
			nome.value = "Ana Maria";
		}
		return { nome, idade, fazerAniversario, mudarNome };
	},
};
</script>
