<template>
    <div class="composition">
        <h2>Composition</h2>
        <h3>{{ counter }}</h3>
        <input class="d-block text-center m-auto mb-3" type="numberic" id="contador" v-model="counter">
        <button class="btn btn-primary ms-3" @click="increment">Incrementar</button>
        <button class="btn btn-primary ms-3" @click="decrease">Disminuir</button>
        <button class="btn btn-success ms-3" @click="double">Multiplicar por 2</button>
        <button class="btn btn-danger ms-3"  @click="reiniciar">Reiniciar</button>
        <p v-if="counter > 10">¡El valor es alto!</p>
    </div>
</template>

<script>
    import { defineComponent, ref } from 'vue';

    export default defineComponent ({
        name: 'CounterComposition',

        setup(){
            const counter = ref(0);

            const increment = () => { counter.value++; }
            const decrease = () => { 
                if(counter.value > 0){
                    counter.value--;
                }
            }
            const double = () => {  counter.value = counter.value*2; }
            const reiniciar = () => { counter.value = 0; }

            return {
                counter, 
                increment,
                decrease,
                double,
                reiniciar
            }
        }
    })
</script>

<style scoped>
    .composition {
        margin: auto;
        width: 60%;
        background-color: rgb(0, 100, 50, 0.2);
        border-radius: 25px;
        margin-bottom: 50px;
        padding: 70px;
   }
</style>