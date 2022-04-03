<script setup lang="ts">
import { ref } from 'vue';
import confetti from 'canvas-confetti';

const duration = ref(10 * 1000);
const end = ref(Date.now() + duration.value);

function startConfetti() {
  // launch a few confetti from the left edge
  confetti({
    particleCount: 7,
    angle: 60,
    spread: 55,
    origin: { x: 0 }
  });
  // and launch a few from the right edge
  confetti({
    particleCount: 7,
    angle: 120,
    spread: 55,
    origin: { x: 1 }
  });

  // keep going until we are out of time
  if (Date.now() < end.value) {
    requestAnimationFrame(startConfetti);
  }
};

</script>

<template>
  <div class="flex justify-center items-center">
    <button @click="startConfetti" class="text-xs font-medium bg-neutral-900 hover:bg-neutral-800 px-3 py-2 rounded-xl">Shoot Confetti <noto-v1:pistol class="ml-1" /></button>
  </div>
</template>