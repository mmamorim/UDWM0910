<template>
    <div class="cxa">
        <div>
            caixa com nome {{ nome }}
        </div>
        <div v-if="contador < 6">
            contador {{ contador }}
            <button @click="incrementa">
                Incrementar
            </button>
        </div>
        <div v-if="contador >= 6">
            <button @click="zerar">
                zerar
            </button>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            contador: 1,
            nome: "Ana"
        }
    },
    methods: {
        incrementa() {
            this.contador++;
        },
        zerar() {
            this.contador = 0;
        }
    },
}
</script>
<style>
.cxa {
    border: 1px solid black;
    padding: 2px;
    margin: 2px;
}
</style>