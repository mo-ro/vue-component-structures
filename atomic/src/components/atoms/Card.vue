<template>
  <div class="todo-card">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.todo-card {
  padding: 15px;
  border-radius: 10px;
  border: 1px solid $light-gray;
  font-size: 12px;
}
</style>
