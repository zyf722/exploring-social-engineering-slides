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
  <div class="slidev-layout">
    <div class="col-header mb-6" :class="props.layoutClass">
      <slot />
    </div>
    <div class="two-columns w-full h-full grid grid-cols-2 grid-rows-2" :class="props.layoutClass">
      <div class="col-top-left" :class="props.class">
        <slot name="topleft" />
      </div>
      <div class="col-top-right" :class="props.class">
        <slot name="topright" />
      </div>
      <div class="col-bottom-left" :class="props.class">
        <slot name="bottomleft" />
      </div>
      <div class="col-bottom-right" :class="props.class">
        <slot name="bottomright" />
      </div>
    </div>
  </div>
</template>
