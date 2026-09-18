<script setup lang="ts">
import { computed, ref } from 'vue'

const count = ref(0)
const doubled = computed(() => count.value *2)
</script>

<template>
  <section id="center">
    <span>Count is {{ count }}</span>
    <button type="button" class="counter" @click="count++">
      +1
    </button>
    <button type="button" class="counter" @click="count--">
      -1
    </button>
    <span>The double of your count is {{ doubled }}</span>
  </section>
</template>
