<script setup>
import Icon from './icons/Icon.vue'

const free = [
  'Registro conversacional ilimitado',
  'Dashboard con gráficos semanales y mensuales',
  'Categorización automática con IA',
]

const pro = [
  'Todo lo del plan Freemium',
  'Detección de Yape/Plin vía Gmail',
  'Proyección de gastos a fin de mes',
  'Metas de ahorro con seguimiento',
  'Alertas y observaciones generadas por IA',
]
</script>

<template>
  <section id="precios" class="bg-paper-soft/60 py-20">
    <div class="mx-auto max-w-6xl px-6">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-extrabold text-navy sm:text-4xl">Empieza gratis, crece a Pro</h2>
        <p class="mt-3 text-navy-soft">Un modelo freemium simple, sin costos ocultos.</p>
      </div>

      <div class="mt-14 grid gap-8 md:grid-cols-2">
        <div class="rounded-3xl bg-white p-8 ring-1 ring-black/5">
          <h3 class="font-display text-xl font-bold text-navy">Freemium</h3>
          <p class="mt-1 text-sm text-navy-soft">Para empezar a ordenar tus gastos hoy mismo.</p>
          <p class="mt-6 text-3xl font-extrabold text-navy">S/ 0</p>
          <ul class="mt-6 space-y-3 text-sm text-navy-soft">
            <li v-for="item in free" :key="item" class="flex items-start gap-2">
              <Icon name="check" class="mt-0.5 h-4 w-4 shrink-0 text-brand" />{{ item }}
            </li>
          </ul>
        </div>

        <div class="rounded-3xl bg-navy-dark p-8 text-white ring-1 ring-black/10">
          <span class="rounded-full bg-brand/20 px-3 py-1 text-xs font-semibold text-brand-light">Recomendado</span>
          <h3 class="mt-3 font-display text-xl font-bold">Pro</h3>
          <p class="mt-1 text-sm text-white/60">Para quienes quieren un asesor financiero con IA.</p>
          <p class="mt-6 text-3xl font-extrabold">Desde S/ 9.90<span class="text-base font-normal text-white/50">/mes</span></p>
          <ul class="mt-6 space-y-3 text-sm text-white/70">
            <li v-for="item in pro" :key="item" class="flex items-start gap-2">
              <Icon name="check" class="mt-0.5 h-4 w-4 shrink-0 text-brand-light" />{{ item }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
