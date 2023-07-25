<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
</template>

<!--
<script lang="ts"> 
    import { defineComponent, Ref, ref } from 'vue'; //defineComponent sew utiliza para defiir un nuevo componente
    export default defineComponent({ 
        //el setup se encarga de realizar las acciones de datos necesarios, definir metodos y funciones
        //ref es una función que se utiliza para crear una refencia reactiva,
        // es decir que se comporta como un objeto reactivo que Vue puede seguur y actualizar automaticamente
        name: 'CounterComposition',
        setup(){
            let counter: Ref = ref(0) //objeto de refencia
            const addCounter = ():void => { 
                counter.value++
                
            }
            return {counter, addCounter}
        }
    })
</script>
-->
<script lang="ts" setup> 
    import { Ref, ref } from 'vue'; 
            let counter: Ref = ref(0)
            const addCounter = ():void => { 
                counter.value++
            }
</script>
