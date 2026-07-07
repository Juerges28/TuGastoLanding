<script setup>
import Icon from './icons/Icon.vue'

const audiences = [
  {
    icon: 'briefcase',
    title: 'Adultos económicamente activos',
    text: 'Profesionales peruanos que quieren claridad sobre en qué se les va el dinero cada mes, sin invertir tiempo en registrarlo.',
  },
  {
    icon: 'graduation-cap',
    title: 'Universitarios y jóvenes profesionales',
    text: 'Quienes empiezan a manejar su propio presupuesto y necesitan una herramienta tan rápida como su ritmo de vida.',
  },
  {
    icon: 'smartphone',
    title: 'Usuarios intensivos de Yape/Plin',
    text: 'Personas que generan un alto volumen de microgastos diarios por billetera digital y no quieren anotar cada uno.',
  },
]
</script>

<template>
  <section class="mx-auto max-w-6xl px-6 py-20">
    <div class="mx-auto max-w-2xl text-center">
      <h2 class="text-3xl font-extrabold text-navy sm:text-4xl">Hecho para tu día a día</h2>
      <p class="mt-3 text-navy-soft">Pensado desde y para el ecosistema financiero peruano.</p>
    </div>

    <div class="mt-14 grid gap-6 md:grid-cols-3">
      <div v-for="a in audiences" :key="a.title" class="rounded-3xl bg-gradient-to-b from-paper-soft to-white p-8 text-center ring-1 ring-black/5">
        <span class="mx-auto flex h-12 w-12 items-center justify-center rounded-2xl bg-white text-brand ring-1 ring-black/5">
          <Icon :name="a.icon" class="h-6 w-6" />
        </span>
        <h3 class="mt-4 font-bold text-navy">{{ a.title }}</h3>
        <p class="mt-2 text-sm leading-relaxed text-navy-soft">{{ a.text }}</p>
      </div>
    </div>
  </section>
</template>
