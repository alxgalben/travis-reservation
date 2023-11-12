<template>
    <div class="todo-item">
      <div class="todo-item-content">
        <div class="todo-item-content-title">
          {{title}}
        </div>
        <div class="todo-item-content-description">
          {{description}}
        </div>
      </div>
    </div>
</template>

<script>
export default {
    props: ['title', 'description']
}
</script>

<style lang="scss" scoped>
.todo {
  &-item {
    background-color: #2c3e50;
    min-height: 70px;
    margin: 10px;
    padding: 10px;
    color: white;

    &-content {
      &-title {
        font-weight: bold;
        font-size: 25px;
      }

      &-description {
        font-size: 20px;
        margin-top: 10px;
      }
    }
  }
}
</style>