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
import { ref } from "vue";
export default {
	components: {
		EmiteEvento,
	},
	setup() {
		let total = ref(0);

		function atualizarTotal(p) {
			const valor = total.value + p;
			total.value = +valor.toFixed(2);
		}

		return { total, atualizarTotal };
	},
};
</script>

<style scoped>
.lista {
	display: flex;
	justify-content: space-between;
}
</style>
