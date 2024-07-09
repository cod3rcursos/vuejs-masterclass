<template>
	<div class="componente">
		<h1>Componente com Propriedades Assistidas</h1>
		<p>Idade: {{ idade }}</p>
		<label>Ano Nascimento:</label>
		<input type="number" v-model="anoNascimento" min="1900" />
		<label>Ano Atual:</label>
		<input type="number" v-model="anoAtual" min="2000" />
	</div>
</template>

<script>
export default {
	data: function () {
		return {
			anoNascimento: 1900,
			anoAtual: 2000,
			idade: 0,
		};
	},
	computed: {
		idade: function () {
			return this.anoAtual - this.anoNascimento;
		},
	},
	watch: {
		anoAtual(novoAno) {
			this.idade = novoAno - this.anoNascimento;
		},
		nascimento(novoNascimento) {
			this.idade = this.anoAtual - novoNascimento;
		},
	},
};
</script>

<style scoped>
label {
	margin: 10px;
}
</style>
