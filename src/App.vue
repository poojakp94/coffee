<template>
  <h1>{{title}}</h1>
  
  <button @click="toggleModal">Click me</button>
  <div v-if="showModal">
  <Modal :header='header' :text="text" theme="sale" @close="toggleModal"/>
  </div>
</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'App',
  components: { Modal},
  data(){
    return {
      title: 'something new',
      header: 'Sign up for the giveaway!',
      text: 'need coffee',
      showModal: false
    }
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
    }
  }
 
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
