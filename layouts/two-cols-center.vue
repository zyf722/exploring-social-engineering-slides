<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
  layoutClass: {
    type: String,
  },
})
</script>

<template>
  <div class="slidev-layout two-columns w-full h-full grid grid-cols-2" :class="props.layoutClass">
    <div class="grid grid-cols-1 h-full place-content-center place-items-center my-auto" :class="props.class">
        <slot />
    </div>
    <div class="grid grid-cols-1 h-full place-content-center place-items-center my-auto" :class="props.class">
        <slot name="right" />
    </div>
  </div>
</template>
