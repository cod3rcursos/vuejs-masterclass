<script>
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import ComDados from "./components/ComDados.vue";
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue";
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue";
import DataBinding from "./components/DataBinding.vue";
import ComProps from "./components/ComProps.vue";
import EscutaEvento from "./components/EscutaEvento.vue";
import PropriedadesComputadas from "./components/PropriedadesComputadas.vue";
import PropriedadesAssistidas from "./components/PropriedadesAssistidas.vue";
import RenderizacaoCondicional from "./components/RenderizacaoCondicional.vue";
import RenderizacaoListas from "./components/RenderizacaoListas.vue";
import Slots from "./components/Slots.vue";

export default {
	data: function () {
		return {
			borracha: "borracha",
			precoBorracha: 2.5,
			cachorrosDoJoao: [
				{ nome: "Totó", idade: 2 },
				{ nome: "Laika", idade: 8 },
				{ nome: "Flor", idade: 6 },
			],
		};
	},
	components: {
		PrimeiroComponente,
		ComDados,
		ComDadosReativosPrimitivos,
		ComDadosReativosNaoPrimitivos,
		DataBinding,
		ComProps,
		EscutaEvento,
		PropriedadesComputadas,
		PropriedadesAssistidas,
		RenderizacaoCondicional,
		RenderizacaoListas,
		Slots,
	},
};
</script>

<template>
	<header>Vue</header>
	<Slots>
		<template v-slot:icone>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="currentColor"
				class="icon icon-tabler icons-tabler-filled icon-tabler-home"
			>
				<path stroke="none" d="M0 0h24v24H0z" fill="none" />
				<path
					d="M12.707 2.293l9 9c.63 .63 .184 1.707 -.707 1.707h-1v6a3 3 0 0 1 -3 3h-1v-7a3 3 0 0 0 -2.824 -2.995l-.176 -.005h-2a3 3 0 0 0 -3 3v7h-1a3 3 0 0 1 -3 -3v-6h-1c-.89 0 -1.337 -1.077 -.707 -1.707l9 -9a1 1 0 0 1 1.414 0m.293 11.707a1 1 0 0 1 1 1v7h-4v-7a1 1 0 0 1 .883 -.993l.117 -.007z"
				/>
			</svg>
		</template>
		<template v-slot:texto> Home </template>
	</Slots>
	<RenderizacaoListas nome="João" :cachorros="cachorrosDoJoao" />
	<RenderizacaoCondicional nome="Maria" :qtde-cachorros="2" />
	<PropriedadesAssistidas />
	<PropriedadesComputadas />
	<EscutaEvento />
	<ComProps :item="borracha" :preco="precoBorracha" />
	<DataBinding />
	<ComDadosReativosNaoPrimitivos />
	<ComDadosReativosPrimitivos />
	<ComDados />
	<PrimeiroComponente />
</template>
