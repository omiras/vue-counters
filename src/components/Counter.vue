<script>
export default {
    props: ['initialValue'],
    emits: ['counterFinished'],
    data() {
        return {
            counter: this.initialValue
        }
    },
    methods: {
        decrement() {
            this.counter--;

            // cuando this.counter ==0 , informaremos al padre de que hemos acabado
            if (this.counter == 0) {
                this.$emit('counterFinished');
            }
        }
    }
}
</script>

<template>
    <article> {{ counter }} </article>
    <button :disabled="counter == 0" @click="decrement"> Decrement </button>
</template>