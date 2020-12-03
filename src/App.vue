<template>
  <div id="app">
    <Kanban :data="data"/>
  </div>
</template>

<script>
import Kanban from"./components/Kanban"

export default {
  name: 'App',
  components: {
    Kanban
  },
  data(){
    return{
      data:[
        {
          name:"todo",
          color:"#FF0066",
          tasks:[]
        },
        {
          name:"todo",
          color:"#33FFCC",
          tasks:[]
        },
        {
          name:"todo",
          color:"#6600CC",
          tasks:[]
        }
      ]
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
}
</style>
