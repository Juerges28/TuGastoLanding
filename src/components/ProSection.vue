<script setup>
import ProScreenMock from './mockups/ProScreenMock.vue'
import Icon from './icons/Icon.vue'

const items = [
  {
    title: 'Proyección de fin de mes',
    text: 'Sabe cuánto vas a gastar y cuánto te quedará antes de que termine el mes.',
  },
  {
    title: 'Metas de ahorro con seguimiento',
    text: 'Define un fondo de emergencia u otra meta y observa tu progreso en tiempo real.',
  },
  {
    title: 'Observaciones generadas por IA',
    text: 'Alertas, sugerencias y reconocimientos sobre tus hábitos, escritos en lenguaje natural.',
  },
]
</script>

<template>
  <section id="pro" class="bg-navy-dark py-20 text-white">
    <div class="mx-auto grid max-w-6xl items-center gap-12 px-6 md:grid-cols-2">
      <div class="order-2 flex justify-center md:order-1 md:justify-start">
        <ProScreenMock />
      </div>

      <div class="order-1 md:order-2">
        <span class="inline-flex items-center gap-2 rounded-full bg-white/10 px-4 py-1.5 text-xs font-semibold text-brand-light">
          TuGasto Pro
        </span>
        <h2 class="mt-5 text-3xl font-extrabold sm:text-4xl">
          Deja que la IA sea tu asesor financiero
        </h2>
        <p class="mt-4 text-white/60">
          En su versión Pro, TuGasto actúa como un asesor que envía alertas
          predictivas y personalizadas de presupuesto, sin que muevas un dedo.
        </p>

        <div class="mt-8 space-y-5">
          <div v-for="item in items" :key="item.title" class="flex gap-4">
            <span class="mt-1 flex h-6 w-6 shrink-0 items-center justify-center rounded-full bg-brand/20 text-brand-light">
              <Icon name="check" class="h-3.5 w-3.5" />
            </span>
            <div>
              <p class="font-semibold">{{ item.title }}</p>
              <p class="mt-1 text-sm text-white/50">{{ item.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
