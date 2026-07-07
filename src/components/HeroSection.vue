<script setup>
import DownloadButtons from './DownloadButtons.vue'
import ChatScreenMock from './mockups/ChatScreenMock.vue'

const highlights = ['Hecho para Perú', 'Integración con Yape/Plin', 'Código abierto']
</script>

<template>
  <section id="top" class="relative overflow-hidden">
    <div class="pointer-events-none absolute -top-32 -right-32 h-96 w-96 rounded-full bg-brand-light/20 blur-3xl"></div>
    <div class="pointer-events-none absolute top-40 -left-32 h-96 w-96 rounded-full bg-navy/5 blur-3xl"></div>

    <div class="mx-auto grid max-w-6xl items-center gap-12 px-6 pb-20 pt-16 md:grid-cols-2 md:pt-24">
      <div>
        <span class="inline-flex items-center gap-2 rounded-full bg-paper-soft px-4 py-1.5 text-xs font-semibold text-brand-dark">
          Registro de gastos conversacional · Zero-UI
        </span>

        <h1 class="mt-5 text-4xl font-extrabold leading-tight text-navy sm:text-5xl">
          Registra tus gastos
          <span class="text-brand">hablando</span>,
          sin formularios.
        </h1>

        <p class="mt-5 max-w-lg text-base leading-relaxed text-navy-soft sm:text-lg">
          TuGasto entiende tu jerga cuando escribes "pan 2 so" y también detecta
          tus Yapes y Plines directo desde Gmail. Sin tipear montos, sin fricción,
          con IA que categoriza todo por ti. Descárgala hoy y pruébala tú mismo.
        </p>

        <div class="mt-8">
          <DownloadButtons />
        </div>

        <div class="mt-8 flex flex-wrap items-center gap-x-6 gap-y-2 text-xs text-navy-soft/80">
          <span v-for="item in highlights" :key="item" class="flex items-center gap-2">
            <span class="h-1.5 w-1.5 shrink-0 rounded-full bg-brand"></span>{{ item }}
          </span>
        </div>
      </div>

      <div class="flex justify-center md:justify-end">
        <ChatScreenMock />
      </div>
    </div>
  </section>
</template>
