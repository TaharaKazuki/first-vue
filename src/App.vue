<template>
  <div id="app">
    <div class="todo-wrapper">
      <div class="todo-container">
        <todo-list :todos="todos" />
        <div class="todo-create-btn-container">
          <div 
            @click="isModalOpen = true"
            class="app-button"
          >
            Create
          </div>
        </div>
      </div>
    </div>
    <Modal 
      @modalClosed="isModalOpen = false"
      :isOpen="isModalOpen" 
    />
  </div>
</template>


<script>
import TodoList from './components/TodoList.vue'
import Modal from './components/Modal.vue'
export default {
  name: 'app',
  components: {
    TodoList,
    Modal
  },
  data() {
    return {
      isModalOpen: false,
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
  },
  // methods: {
  //   openModal() {
  //     this.isModalOpen = !this.isModalOpen
  //   }
  // }
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

.app-button {
  font-size: 20px;
  padding: 10px;
  border-radius: 5px;
  background-color: #795899;
  color: white;
  font-weight: bold;
  &:hover {
    cursor: pointer;
  }
}

.todo {
  &-wrapper {
    display: flex;
    justify-content: center;
    width: 100%;
  }
  &-create-btn-container {
    margin: 10px;
  }
  &-container {
    display: flex;
    flex-direction: column;
    width: 400px;
    min-height: 400px;
    background-color: #ededed;
    border-radius: 5px;
  }
}

</style>
