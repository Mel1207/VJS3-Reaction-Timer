<template>
  <h1>Reaction Timer</h1>
  <button @click="start" class="btn" :disabled="isPlaying">Play</button>
  <Block v-if="isPlaying" :delay="delay" />
</template>

<script>
import Block from './components/Block.vue'

export default {
  components: { Block },
  data() {
    return {
      isPlaying: false,
      delay: null
    }
  },
  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000
      this.isPlaying = true
      // console.log(this.delay)
    }
  }
}
</script>
