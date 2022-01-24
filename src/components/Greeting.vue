<template>
  <card>
    <h2 class="is-size-3">HI <span class="username">{{ displayName }},</span></h2>
    <span class="is-size-1">WELCOME BACK 👋</span>
  </card>
</template>

<script>
import Card from './Card.vue'

export default {
  name: 'Greeting',

  components: { Card },

  props: {
    username: String
  },

  computed: {
    displayName () {
      return this.username.toUpperCase();
    }
  }
}
</script>

<style scoped>
h2, .is-size-1 {
  color: #04446B !important;
  font-weight: 700;
}
</style>