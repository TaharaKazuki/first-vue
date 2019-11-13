<template>
  <div id="app">
    <div class='todo-wrapper'>
      <div class='todo-container'>
        <todo-list :todos="todos"/>
      </div>
    </div>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
export default {
  name: 'app',
  components: {
    TodoList
  },
  data() {
    return {
      todos: [
        {
          _id: '1',
          title: '犬の散歩',
          description: '近くの動物園'
        },
        {
          _id: '2',
          title: 'パンを買う',
          description: '全粒粉のパンがおすすめ'
        },
        {
          _id: '3',
          title: 'プログラミングをする',
          description: '明日も好調'
        }
      ]
    }
  }
}
</script>

<style lang='scss'>
$color-red: red;


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.todo {
  &-wrapper {
    display: flex;
    justify-content: center;
    width: 100%;
  }
  &-container {
    width: 400px;
    min-height: 400px;
    background-color: #ededed;
    border-radius: 5px;
  }
}

</style>
