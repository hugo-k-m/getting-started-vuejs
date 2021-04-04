<template>
  <div id="app">
    <h1>My TS App</h1>
    <p><input type="text" v-model="inputText" /></p>
    <p>Count: {{ count }}</p>
    <p><button @click="reset()">Reset</button></p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  data: () => {
    return { inputText: '' }
  },
  methods: {
    reset(){
      this.inputText = ''
    }
  },
  computed: {
    count() {
      return this.inputText.length
    }
  }
});
</script>