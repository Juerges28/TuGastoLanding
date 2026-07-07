<script setup>
import Icon from '../icons/Icon.vue'

defineProps({
  dark: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <div class="relative mx-auto w-[260px] select-none sm:w-[280px]">
    <div
      class="relative overflow-hidden rounded-[2.5rem] border-[6px] shadow-2xl"
      :class="dark ? 'border-neutral-900 bg-navy-dark' : 'border-neutral-900 bg-paper'"
    >
      <div class="absolute left-1/2 top-0 z-20 h-5 w-24 -translate-x-1/2 rounded-b-2xl bg-neutral-900" />
      <div class="flex items-center justify-between px-5 pb-1 pt-2.5 text-[10px] font-semibold" :class="dark ? 'text-white' : 'text-navy'">
        <span>7:31</span>
        <span class="flex items-center gap-1.5">
          <Icon name="wifi" class="h-3 w-3" />
          <Icon name="battery" class="h-3.5 w-3.5" />
        </span>
      </div>
      <div class="h-[460px] overflow-hidden">
        <slot />
      </div>
    </div>
  </div>
</template>
