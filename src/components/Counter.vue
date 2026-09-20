<script setup lang="ts">
import { computed, ref } from 'vue'

const count = ref(0)
const doubled = computed(() => count.value *2)
</script>

<template>
  <section id="center">
    <h1>Simple counter</h1>
    <h2>Count is {{ count }}</h2>
    <div class="buttons">
    <button type="button" class="counter" @click="count++">
      +1
    </button>
    <button type="button" class="counter" @click="count--">
      -1
    </button>
    </div>
    <p>Fun fact: The double of {{ count }} is {{ doubled }}</p>
    <button type="button" @click="count=0">
      Reset
    </button>
  </section>
</template>

<style scoped>
.buttons {
  display:flex;
  gap: 10px;
}
</style>

