<template>
    <div class="option">
        <h2>Option</h2>
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
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'CounterOption',

        data() {
                let counter = 0;
                return { counter };
        },

        methods: {
            increment() {
                this.counter++;
            },

            decrease() {
                if(this.counter > 0){
                    this.counter--;
                }
            },

            double() {
                this.counter *= 2;
            },

            reiniciar() {
                this.counter = 0;
            }
        }
    })
</script>

<style scoped>
   .option {
        margin: auto;
        width: 60%;
        background-color: rgb(0, 50, 200, 0.2);
        border-radius: 25px;
        margin-bottom: 50px;
        padding: 70px;
   }
</style>