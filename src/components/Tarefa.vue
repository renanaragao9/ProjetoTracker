<template>
    <div class="box">
        <div class="columns">
            <div class="column is-7">
                {{tarefa.descricao}}
            </div>
            <div class="column">
                <Cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import Cronometro from './Cronometro.vue';
import ITarefa from '../interfaces/ITarefas';

export default defineComponent ({
    name: 'TarefaProjeto',
    
    components: {
        Cronometro,
    },

    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
                Required: true
        }
    }


})
</script>

<style scoped>
    .box {
        background: #fafafa;
        color: #000;
        font-weight: bold
    }
</style>