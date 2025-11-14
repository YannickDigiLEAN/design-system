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
  <div class="slidev-layout three-columns w-full h-full" :class="props.layoutClass">
    <div :class="props.class">
      <slot />
    </div>
    <div class="grid grid-cols-3 gap-8">
    <div class="col-left" :class="props.class">
      <slot name="left" />
    </div>
    <div class="col-center" :class="props.class">
      <slot name="center" />
    </div>
    <div class="col-right" :class="props.class">
      <slot name="right" />
    </div>
    </div>
    
  </div>
</template>