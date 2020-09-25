<template>
  <div class="button" role="button" @click="$emit('click')">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.button {
  font-size: 12px;
  padding: 12px 8px;
  background-color: $light-gray;
  cursor: pointer;
}
</style>
