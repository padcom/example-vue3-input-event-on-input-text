<template>
  <h1>Hello, world! {{ message }} {{ text }}</h1>
  <input v-model="text" type="text" @input="console.log('input type=text:', $event)">
  <textarea v-model="text" @input="console.log('textarea:', $event)" />
</template>

<script lang="ts" setup>
import { ref } from 'vue'

defineProps({
  message: { type: String, default: 'from HelloWorld.vue' },
})

const text = ref('change me')
</script>

<style lang="postcss" scoped>
h1 {
  font-size: 1.875rem;
  line-height: 2.25rem;
}
</style>
