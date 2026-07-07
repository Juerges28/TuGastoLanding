<script setup>
import Icon from './icons/Icon.vue'
import { GITHUB_REPO_URL, GITHUB_RELEASE_URL } from '../constants'

defineProps({
  variant: {
    type: String,
    default: 'light',
  },
})
</script>

<template>
  <div class="w-full max-w-md">
    <div class="flex flex-col gap-3 sm:flex-row">
      <a
        :href="GITHUB_RELEASE_URL"
        target="_blank"
        rel="noopener noreferrer"
        class="inline-flex items-center justify-center gap-2 rounded-full bg-brand px-6 py-3 text-sm font-semibold text-white transition hover:bg-brand-dark active:scale-[0.98]"
      >
        <Icon name="download" class="h-4 w-4" />
        Descargar APK
      </a>
      <a
        :href="GITHUB_REPO_URL"
        target="_blank"
        rel="noopener noreferrer"
        class="inline-flex items-center justify-center gap-2 rounded-full border px-6 py-3 text-sm font-semibold transition"
        :class="variant === 'dark'
          ? 'border-white/20 text-white hover:bg-white/10'
          : 'border-black/10 text-navy hover:bg-paper-soft'"
      >
        <Icon name="github" class="h-4 w-4" />
        Ver en GitHub
      </a>
    </div>
    <p class="mt-2 text-xs" :class="variant === 'dark' ? 'text-white/50' : 'text-navy-soft/70'">
      Código abierto · Publicado como GitHub Release · Android 8.0+
    </p>
  </div>
</template>
