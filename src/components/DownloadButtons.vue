<script setup>
import Icon from './icons/Icon.vue'
import { APK_DOWNLOAD_URL, APKPURE_URL } from '../constants'

defineProps({
  variant: {
    type: String,
    default: 'light',
  },
})
</script>

<template>
  <div class="flex flex-col items-center gap-3 w-full max-w-md">
    <!-- GitHub Releases -->
    <a
      :href="APK_DOWNLOAD_URL"
      target="_blank"
      rel="noopener noreferrer"
      class="inline-flex w-full items-center justify-center gap-2 rounded-full bg-brand px-6 py-3 text-sm font-semibold text-white transition hover:bg-brand-dark active:scale-[0.98]"
    >
      <Icon name="github" class="h-4 w-4" />
      Descargar APK (GitHub)
    </a>

    <!-- APKPure -->
    <a
      :href="APKPURE_URL"
      target="_blank"
      rel="noopener noreferrer"
      class="inline-flex w-full items-center justify-center gap-2 rounded-full border-2 border-brand px-6 py-3 text-sm font-semibold transition active:scale-[0.98]"
      :class="variant === 'dark' ? 'text-white hover:bg-white/10' : 'text-brand hover:bg-brand/5'"
    >
      <Icon name="apkpure" class="h-4 w-4" />
      Descargar en APKPure
    </a>

    <p class="mt-1 text-xs" :class="variant === 'dark' ? 'text-white/50' : 'text-navy-soft/70'">
      Instalación directa · Android 8.0+
    </p>
  </div>
</template>

