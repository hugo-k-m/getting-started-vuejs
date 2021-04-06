<template>
  <div -d="char-count">
    <p>{{ label }}: {{ count }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'CharCount',
  props: {
    inputText: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true,
    }
  },
  computed: {
    count(): number {
      return this.inputText.length
    }
  }
});
</script>

<style lang="scss" scoped></style>