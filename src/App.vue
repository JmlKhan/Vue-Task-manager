<template>
  <div class="container">
    
    <Header @toggle-add-task="toggleAddTask" title="Task tracker"
    :showAddTask="showAddTask"
    />
    
    <router-view :showAddTask="showAddTask"/>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Header,
    Footer
  },
  data() {
    return{
      showAddTask: false,
    }
  },
  methods: {
 
    toggleAddTask() {
      this.showAddTask = !this.showAddTask
    },
    
  },
  
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
  width: 400px;
  
  height: 500px;
}
#container {
 border: 1px solid black;
 
}


</style>
