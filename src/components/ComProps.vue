<template>
	<div class="componente">
		<h1>Componente com Props</h1>
		<p>{{ item }} (R${{ preco.toFixed(2) }})</p>
	</div>
</template>

<script>
export default {
	props: ["item", "preco"],
	data: function () {
		return {};
	},
};
</script>
