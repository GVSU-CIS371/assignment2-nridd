<script setup lang="ts">
import { computed } from "vue"

const props = defineProps<{ base: string }>()

const baseClass = computed(() => {
  switch (props.base) {
    case "Coffee":
      return "coffee"
    case "Green Tea":
      return "green-tea"
    case "Black Tea":
      return "black-tea"
    default:
      return ""
  }
})
</script>

<template>
  <div class="base" :class="baseClass"></div>
</template>

<style scoped>
.base {
  width: 100%;
  height: 60%;
  border-radius: 6px;
  box-shadow: inset 0 0 6px rgba(0,0,0,.25);
}
.coffee { background: #5a381e; }
.green-tea { background: #cfe2a9; }
.black-tea { background: #9b5c15; }
</style>
