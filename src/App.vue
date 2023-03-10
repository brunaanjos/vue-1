<script >
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
      if( this.contador > 0){
      this.contador--
      }
    },
    reiniciarConatdor(){
      this.contador = 0
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}

</script>

<template>
  <button @click="reiniciarConatdor">reiniciar</button>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <p>Valor do contador é: {{ contador }}</p>
</template>   

<style scoped>
button {
  font-weight: bold;
}
</style>
