<script setup>
import { ref } from 'vue'
import AppLogo from './AppLogo.vue'
import Icon from './icons/Icon.vue'
import { GITHUB_RELEASE_URL } from '../constants'

const open = ref(false)

const links = [
  { label: 'Cómo funciona', href: '#como-funciona' },
  { label: 'Funciones', href: '#funciones' },
  { label: 'Pro', href: '#pro' },
  { label: 'Precios', href: '#precios' },
  { label: 'Descargar', href: '#descargar' },
]

function closeMenu() {
  open.value = false
}
</script>

<template>
  <header class="sticky top-0 z-50 border-b border-black/5 bg-paper/85 backdrop-blur">
    <div class="mx-auto flex max-w-6xl items-center justify-between px-6 py-4">
      <a href="#top">
        <AppLogo />
      </a>

      <nav class="hidden items-center gap-8 md:flex">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="text-sm font-medium text-navy-soft transition hover:text-brand"
        >
          {{ link.label }}
        </a>
      </nav>

      <a
        :href="GITHUB_RELEASE_URL"
        target="_blank"
        rel="noopener noreferrer"
        class="hidden items-center gap-2 rounded-full bg-brand px-5 py-2.5 text-sm font-semibold text-white transition hover:bg-brand-dark md:inline-flex"
      >
        <Icon name="download" class="h-4 w-4" />
        Descargar APK
      </a>

      <button
        class="flex h-9 w-9 items-center justify-center rounded-lg border border-black/10 text-navy md:hidden"
        @click="open = !open"
        aria-label="Abrir menú"
      >
        <Icon :name="open ? 'close' : 'menu'" class="h-5 w-5" />
      </button>
    </div>

    <div v-if="open" class="border-t border-black/5 bg-paper px-6 py-4 md:hidden">
      <nav class="flex flex-col gap-4">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="text-sm font-medium text-navy-soft"
          @click="closeMenu"
        >
          {{ link.label }}
        </a>
        <a
          :href="GITHUB_RELEASE_URL"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center justify-center gap-2 rounded-full bg-brand px-5 py-2.5 text-center text-sm font-semibold text-white"
          @click="closeMenu"
        >
          <Icon name="download" class="h-4 w-4" />
          Descargar APK
        </a>
      </nav>
    </div>
  </header>
</template>
