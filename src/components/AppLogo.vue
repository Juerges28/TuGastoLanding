<script setup>
defineProps({
  dark: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <span class="flex items-center gap-2">
    <svg viewBox="0 0 64 64" class="h-8 w-8 shrink-0" xmlns="http://www.w3.org/2000/svg">
      <defs>
        <linearGradient id="logo-gradient" x1="0" y1="0" x2="1" y2="1">
          <stop offset="0" stop-color="#34D9A6" />
          <stop offset="1" stop-color="#0E7C63" />
        </linearGradient>
      </defs>
      <path
        d="M14 10h36a8 8 0 0 1 8 8v20a8 8 0 0 1-8 8H30l-10 8v-8h-6a8 8 0 0 1-8-8V18a8 8 0 0 1 8-8z"
        fill="url(#logo-gradient)"
      />
      <path d="M22 26h16M22 33h11" stroke="#fff" stroke-width="3.2" stroke-linecap="round" fill="none" />
      <path d="M37 40l4-8 4 5 6-10" stroke="#fff" stroke-width="3.2" fill="none" stroke-linecap="round" stroke-linejoin="round" />
    </svg>
    <span class="font-display text-lg font-bold" :class="dark ? 'text-white' : 'text-navy'">
      <span class="text-brand-mid">Tu</span>Gasto
    </span>
  </span>
</template>
