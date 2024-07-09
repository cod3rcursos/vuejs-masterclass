<template>
	<div class="componente">
		<h1>Componente Com Dados Reativos Primitivos</h1>
		<p>Nome: {{ nome }} | Idade: {{ idade }}</p>
		<button v-on:click="fazerAniversario">Fazer Aniversário</button>
		<button @click="mudarNome()">Mudar Nome</button>
	</div>
</template>

<script>
export default {
	data: function () {
		return {
			nome: "Ana",
			idade: 26,
		};
	},
	methods: {
		fazerAniversario() {
			this.idade++;
		},
		mudarNome() {
			this.nome = "Ana Maria";
		},
	},
};
</script>
