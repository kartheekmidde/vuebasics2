<template>
  <h1>{{ title }}</h1>
  <p>Welcome..</p>
  <teleport to=".modals" v-if="showModal">
    <Modal :header="headerTxt" :text="textVal" theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Sign up now</a>
        <a href="#">More info</a>
      </template>
      <h1>Heading slot</h1>
      <p>Test para slot</p>
    </Modal>
  </teleport>

  <teleport to=".modals" v-if="showModal2">
    <Modal theme="sale" @close="toggleModal2">
      <h1>Different slot</h1>
      <p>Different para</p>
    </Modal>
  </teleport>
  <button @click="toggleModal">open modal</button>
  <button @click="toggleModal2">open modal2</button>
</template>

<script>
import Modal from './components/Modal';

export default {
  name: 'App',
  components: {
    Modal
  },
  data(){
    return {
      title: 'My First Vue App',
      headerTxt: 'Sign up',
      textVal: 'Forgot your password',
      showModal: false,
      showModal2: false,
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModal2(){
      this.showModal2 = !this.showModal2;
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
  margin-top: 60px;
}
</style>
