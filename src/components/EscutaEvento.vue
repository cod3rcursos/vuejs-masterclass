<template>
	<div class="componente">
		<h1>Componente que Escuta Evento</h1>
		<p>Total: R${{ total }}</p>
		<div class="lista">
			<EmiteEvento item="Item1" :preco="1.99" @foiAdicionado="atualizarTotal" />
			<EmiteEvento item="Item2" :preco="5.0" @foiAdicionado="atualizarTotal" />
			<EmiteEvento
				item="Item3"
				:preco="10.99"
				@foiAdicionado="atualizarTotal"
			/>
		</div>
	</div>
</template>

<script>
import EmiteEvento from "./EmiteEvento.vue";

export default {
	data: function () {
		return {
			total: 0,
		};
	},
	components: {
		EmiteEvento,
	},
	methods: {
		atualizarTotal(valor) {
			const novo = this.total + valor;
			this.total = parseFloat(novo.toFixed(2));
		},
	},
};
</script>

<style scoped>
.lista {
	display: flex;
	justify-content: space-between;
}
</style>
