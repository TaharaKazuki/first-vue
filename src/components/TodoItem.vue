<template>
  <div class='todo-item'>
    <div class='todo-itme-content-title'>
      犬の散歩
    </div>
    <div class='todo-item-content-description'>
      動物園の近くまで行く
    </div>
  </div>
</template>
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