<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <input type="text" v-model="info" >
    <button @click="handlerclick">提交</button>
    <ul>
      <todu v-for="item in list" :key="item" :item="item"></todu>
    </ul>
  </div>
</template>

<script>
import todu from './components/todu.vue'

export default {
  name: 'app',
  data () {
    return {
      list:[],
      info:''
    }
  },
  methods:{
    handlerclick(){
      this.list.push(this.info)
      this.info = ''
    }
  },
  components: {
    todu
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
