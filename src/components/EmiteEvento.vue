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
	setup(props, { emit }) {
		let item = props.item;
		let preco = props.preco;

		function adicionar() {
			emit("foiAdicionado", preco);
		}
		return { item, preco, adicionar };
	},
};
</script>
