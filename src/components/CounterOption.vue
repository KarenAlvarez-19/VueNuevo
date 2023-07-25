<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
</template>

<script lang="ts">
    import { defineComponent} from 'vue'; //el defineComponer sirve para definir el componente y los primero que se hace es importarlo  
    export default defineComponent({ //para poder usarlo se tiene que exportar y posteriormente se definen objetos
        name:'CounterOption',
        components:{}, //se colocan los componentes que se van a utilizar y se tienen que importar
        data(){ //data es una funcion que retorna los datos
            let counter = 0;
            return {counter}
        },//definir datos o variables que vamos a tener en nuestro componente
        methods:{
            addCounter(){
                this.counter++ //para acceder a los datos, se ocupa this
            }
        }
    })
</script>

<style>
</style>