<template>
  <div>
    <h1>{{ title }}</h1>
    <div v-if="this.showModal">
       <Modal :header="this.header" :text="this.text" theme="sale" @close="this.toggleModal"/>
    </div>
    <br>
    <button @click="toggleModal">
        Open modal
    </button>
  </div>
  
</template>

<script>
import Modal from './components/Modal';


export default {
  name: 'App',
  components: {
    Modal,
  },
  data () {
    return{
      title : 'Standard Modal',
      header: "Sign up for the holiday promo",
      text: "Grab yours now",
      showModal : false,
    }
  },
  methods : {
    handleClick(){
      this.$refs.name.classList.toggle('active');
      this.$refs.name.focus();
    },
    toggleModal() {
      this.showModal = !this.showModal;
    },
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
  margin-top: 60px;

}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
