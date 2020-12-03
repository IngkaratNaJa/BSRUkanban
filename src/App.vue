<template>
  <div id="app">
    <Kanban :data="data" :create_task_submit="create_task_submit"/>
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
          tasks:[
            {
              task_name:"aaaa"
            }
          ]
        },
        {
          name:"doing",
          color:"#33FFCC",
          tasks:[
            {
              task_name:"bbbb"
            }
          ]
        },
        {
          name:"done",
          color:"#6600CC",
          tasks:[
            {
              task_name:"cccc"
            }
          ]
        }
      ]
    }
  },
  methods:{
    create_task_submit(column_index,item){
      this.data[column_index].tasks.push(item)
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
  color: black;
}
</style>
