<template>
  <div class="card">
    <div class="card-content" :style="styling">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  
  props: {
    padding: {
      type: Number,
      required: false,
      default: 24,
    }
  },

  computed: {
    styling () {
      return `padding: ${this.padding}px`;
    }
  }
}
</script>