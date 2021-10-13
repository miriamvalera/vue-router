<template>
    <h1>About Page</h1>
    <hr>
    <h2>{{ name }}</h2>
    <button @click="onChangeName">
        Cambiar nombre
    </button>
</template>

<script>
export default {
    data() {
        return  {
            name: 'Miriam'
        }
    },

    methods: {
        onChangeName() {
            // console.log('Se cambiará el nombre a Jose')
            this.name = 'Jose'
            // console.log(this.name)
        }
    }, 

    beforeCreate() {  // se suele utilizar para realizar validaciones antes de montar componentes
        console.log('beforeCreate')
    },
    created() { // se suelen hacer las peticiones HTTP que se necesiten ya que el componente esta montado y data tiene valores
        this.name = 'Alexandra'
        console.log('created')
    },
    beforeMount() {
        console.log('beforeMount')
    },
    mounted() {
        console.log('mounted')
    },
    beforeUpdate() {
        console.log('beforeUpdate')
    },
    updated() {
        console.log('updated')
    },
    activated() {
        console.log('activated')
    },
    deactivated() {
        console.log('deactivated')
    },
    beforeUnmount() {
        console.log('beforeUnmount')
    },
    unmounted() { // se suele utilizar para hacer limpieza
        console.log('unmounted')
    },
    errorCaptured() {
        console.log('errorCaptured')
    },
    renderTracked() {
        console.log('renderTracked')
    },
    renderTriggered() {
        console.log('renderTriggered')
    },
}
</script>