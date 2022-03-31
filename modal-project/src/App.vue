<template>
  <h1> {{ title }} </h1>
  <p>Welcome...</p>
<div v-if="showModal">  <Modal  @close="toggleModal"/></div>
<button @click="toggleModal">Open Modal</button>
 <!-- <div class="container"> 
      <button @click="back"><i class='bx bx-left-arrow-alt bx-fade-left-hover' ></i></button>
      <button @click="redirect"><i class='bx bxs-home' ></i></button>
      <button @click="forward"><i class='bx bx-right-arrow-alt bx-fade-right-hover'></i></button> 
     </div> -->
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
data(){
  return{
    title:'Enjoying the vue',
    showModal:false,
    showModalTwo:false,
  }
},
methods: {
  toggleModal(){
    this.showModalTwo = !this.showModalTwo
  },
  toggleModal(){
    this.showModalTwo = !this.showModalTwo
  }
},
redirect(){
       this.$router.push({name:'Home'})
    },
    back(){
      this.$router.go(-1)
    },
    forward(){
       this.$router.go(1)
    }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
 
}
       h1{
            border-bottom: 1px solid rgb(73, 53, 37);
            display:inline-block;
            padding-bottom: 10px;
            color: crimson;
            width: 400px;
            padding: 20px;
            margin: 100px auto;
          background: white;
          }

</style>
