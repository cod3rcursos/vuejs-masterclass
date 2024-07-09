<template>
    <div class="componente">
        <h1>Componente com Slots</h1>
        <button> 
            <slot name="icone"/> 
            <slot name="texto">
                Botão
            </slot>
        </button>
    </div>
</template>