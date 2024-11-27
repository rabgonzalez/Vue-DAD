<template>
    <div class="container">
        <div class="row">
            <h2>Composition</h2>
            <h3>{{ counter }}</h3>
        </div>

        <div class="row">
            <div class="col-12">
                <input class="d-block text-center m-auto" type="numberic" id="contador" v-model="counter">
            </div>
            <div class="col-12 col-md">
                <button class="btn btn-primary" @click="increment">Incrementar</button>
            </div>
            <div class="col-12 col-md">
                <button class="btn btn-primary" @click="decrease">Disminuir</button>
            </div>
            <div class="col-12 col-md">
                <button class="btn btn-success" @click="double">Multiplicar por 2</button>
            </div>
            <div class="col-12 col-md w-100">
                <button class="btn btn-danger" @click="reiniciar">Reiniciar</button>
            </div>
            <p v-if="counter > 10">¡El valor es alto!</p>
        </div>
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