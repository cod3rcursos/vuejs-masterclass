<template>
	<div class="componente">
		<h1>Componente com Renderização Condicional</h1>
		<p>Nome : {{ nome }}</p>
		<p v-if="qtdeCachorros === 0">Não tem Cachorros</p>
		<p v-else-if="qtdeCachorros === 1">Tem um Cachorro</p>
		<p v-else>Tem muitos Cachorros</p>
	</div>
</template>

<script>
export default {
	props: ["nome", "qtdeCachorros"],
	setup(props) {
		return { ...props };
	},
};
</script>
