<template>
	<div class="componente">
		<h1>Componente que Emite Evento</h1>
		<p>{{ item }} (R${{ preco.toFixed(2) }})</p>
		<button @click="adicionar">Adicionar ao carrinho</button>
	</div>
</template>

<script>
export default {
	props: ["item", "preco"],
	data: function () {
		return {};
	},
	methods: {
		adicionar() {
			this.$emit("foiAdicionado", this.preco);
		},
	},
};
</script>
