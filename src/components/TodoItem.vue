<template>
  <div class='todo-item'>
    <div class='todo-itme-content-title'>
      {{ title }}
    </div>
    <div class='todo-item-content-description'>
      {{ description }}
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true,
      default: 'Default Description'
    }
  }
}
</script>
<style lang="scss">
  .todo {
    &-item {
      background-color: gray;
      min-height: 70px;
      margin: 10px;
      padding: 10px;
      color: white;
      border-radius: 5px;
      font-size: 23px;
    }
    &-itme-content-title {
      font-weight: bold;
    }
    &-item-content-description {
      font-size: 19px;
    }
  }
</style>