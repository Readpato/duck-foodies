<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
const buttons = [
  {
    id: 'decrement',
    onClick: () => count.value--,
    order: 'order-0',
    text: '-',
  },
  {
    id: 'increment',
    onClick: () => count.value++,
    order: 'order-2',
    text: '+',
  },
]
</script>

<template>
  <div
    aria-label="counter"
    flex="~ justify-center items-center gap-4" mt-2 text-center
  >
    <button
      v-for="{ id, onClick, order, text } in buttons" :key="id"
      :aria-label="`${id}-counter`"
      :class="`${order}`"
      :data-test="`${id}-cta`"
      w-8 h-8
      hover="bg-white text-black"
      border="2 green rounded"
      @click="onClick"
    >
      {{ text }}
    </button>
    <span
      w-fit min-w-5 order-1
      aria-label="counter-value"
      data-test="counter-value"
    >{{ count }}
    </span>
  </div>
</template>
