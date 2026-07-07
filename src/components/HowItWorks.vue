<script setup>
import Icon from './icons/Icon.vue'

const steps = [
  {
    n: '01',
    title: 'Escribe o deja que la IA lo detecte',
    text: 'Escribe algo tan simple como "pan 2 so" en el chat, o deja que TuGasto intercepte tus recibos de Yape/Plin desde tu correo automáticamente.',
    icon: 'chat',
  },
  {
    n: '02',
    title: 'La IA categoriza al instante',
    text: 'Groq procesa el lenguaje natural en milisegundos y asigna monto, categoría y fecha sin que tengas que llenar un solo campo.',
    icon: 'sparkles',
  },
  {
    n: '03',
    title: 'Visualiza todo en tu dashboard',
    text: 'Consulta gráficos dinámicos por semana o mes y, con TuGasto Pro, recibe proyecciones y alertas antes de que se acabe tu presupuesto.',
    icon: 'chart-bar',
  },
]
</script>

<template>
  <section id="como-funciona" class="mx-auto max-w-6xl px-6 py-20">
    <div class="mx-auto max-w-2xl text-center">
      <h2 class="text-3xl font-extrabold text-navy sm:text-4xl">Cómo funciona</h2>
      <p class="mt-3 text-navy-soft">
        De tu bolsillo a tu dashboard en tres pasos, sin abrir un formulario.
      </p>
    </div>

    <div class="mt-14 grid gap-8 md:grid-cols-3">
      <div v-for="step in steps" :key="step.n" class="relative rounded-3xl bg-white p-8 shadow-sm ring-1 ring-black/5">
        <span class="flex h-11 w-11 items-center justify-center rounded-xl bg-paper-soft text-brand">
          <Icon :name="step.icon" class="h-5 w-5" />
        </span>
        <span class="absolute right-6 top-6 font-display text-2xl font-extrabold text-paper-soft">{{ step.n }}</span>
        <h3 class="mt-5 text-lg font-bold text-navy">{{ step.title }}</h3>
        <p class="mt-2 text-sm leading-relaxed text-navy-soft">{{ step.text }}</p>
      </div>
    </div>
  </section>
</template>
