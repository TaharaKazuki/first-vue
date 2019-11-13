<template>
  <div class='todo-list'>
    <todo-item
    v-bind:title="'犬の散歩'"
    v-bind:description="'近くの動物園'"
    />
    <todo-item
    :title="'パンを買う'"
    :description="'全粒粉のパンがおすすめ'"
    />
    <todo-item 
    :title=todoTitle
    :description=todoDescription
    />
  </div>
</template>
<script>
import TodoItem from '../components/TodoItem.vue'

export default {
  components: {
    TodoItem
  },
  data() {
    return {
      todoTitle: 'プログラミング学習',
      todoDescription: '明日が最高'
    }
  }
}
</script>