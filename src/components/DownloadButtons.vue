<script setup>
import Icon from './icons/Icon.vue'
import { APK_DOWNLOAD_URL } from '../constants'

defineProps({
  variant: {
    type: String,
    default: 'light',
  },
})
</script>

<template>
  <div class="w-full max-w-md">
    <a
      :href="APK_DOWNLOAD_URL"
      class="inline-flex items-center justify-center gap-2 rounded-full bg-brand px-6 py-3 text-sm font-semibold text-white transition hover:bg-brand-dark active:scale-[0.98]"
    >
      <Icon name="download" class="h-4 w-4" />
      Descargar APK
    </a>
    <p class="mt-2 text-xs" :class="variant === 'dark' ? 'text-white/50' : 'text-navy-soft/70'">
      Instalación directa · Android 8.0+
    </p>
  </div>
</template>
