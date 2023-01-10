<template>
    <Box>
        <div class="conlums is-flex is-justify-content-space-between">
            <div class="column is-7">
                {{tarefa.descricao || 'Tarefa sem descrição'}}
            </div>
            <div class="column">
                <Cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
            </div>
        </div>
    </Box>
</template>

<script lang="ts">

import { defineComponent, PropType } from "vue";
import Cronometro from './Cronometro.vue';
import ITarefa from "../Interfaces/ITarefa";
import Box from "./Box.vue";

export default defineComponent({
    name: 'Tarefa-nome',
    components: {
        Cronometro,
        Box
    },
    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
            require: true
        }
    }
})
</script>

