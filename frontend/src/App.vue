<template>
  <div id="app">
    <h1>Crypto Visualizer</h1>
    <Base64Tool />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Base64Tool from './components/Base64Tool.vue'

export default defineComponent({
  name: 'App',
  components: { Base64Tool }
})
</script>
