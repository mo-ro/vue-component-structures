<template>
  <div
    :class="`icon-button mdi mdi-${icon} -${size}`"
    @click="$emit('click')"
  ></div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'nuxt-property-decorator';

@Component
export default class IconButton extends Vue {
  @Prop({ required: true })
  icon!: string;

  @Prop({ default: 'medium' })
  size!: string;
}
</script>

<style lang="scss" scoped>
.icon-button {
  cursor: pointer;
  border-radius: 100%;
  box-sizing: content-box;
  padding: 8px;

  &:hover {
    background-color: $light-gray;
  }

  &.-small {
    font-size: 18px;
    width: 18px;
    height: 18px;
  }

  &.-medium {
    font-size: 24px;
    width: 24px;
    height: 24px;
  }

  &.-large {
    font-size: 32px;
    width: 32px;
    height: 32px;
  }
}
</style>
