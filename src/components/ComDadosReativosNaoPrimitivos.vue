<template>
	<div class="componente">
		<h1>Componente Com Dados Reativos Não Primitivos</h1>
		<p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
		<button @click="fazerAniversario">Fazer Aniversário</button>
		<button @click="mudarNome()">Mudar Nome</button>
	</div>
</template>

<script>
import { reactive } from "vue";
export default {
	setup: function () {
		const pessoa = reactive({ nome: "Ana", idade: 27 });

		function fazerAniversario() {
			pessoa.idade += 1;
		}

		function mudarNome() {
			pessoa.nome = "Ana Maria";
		}
		return { pessoa, fazerAniversario, mudarNome };
	},
};
</script>
