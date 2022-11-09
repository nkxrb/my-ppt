<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground } from '../layoutHelper'
import bgImg from '../image/cover.jpeg';

const props = defineProps({
  background: {
    // random image from a curated Unsplash collection by Anthony
    default: bgImg,
  },
})

const style = computed(() => handleBackground(props.background, true))
</script>

<template>
  <div
    class="slidev-layout cover text-center"
    :style="style"
  >
    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>
