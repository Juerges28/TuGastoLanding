<script setup>
import AppLogo from './AppLogo.vue'

const team = ['Escobedo Ocaña, Jorge Luis', 'Gordillo Mendoza, Jose Alonzo', 'Roque Quisipe, William Isaias']
</script>

<template>
  <footer class="bg-navy-dark py-12 text-white/70">
    <div class="mx-auto max-w-6xl px-6">
      <div class="flex flex-col items-start justify-between gap-8 sm:flex-row">
        <div>
          <a href="#top">
            <AppLogo dark />
          </a>
          <p class="mt-3 max-w-xs text-sm">
            Registro conversacional de gastos con IA, pensado para el ecosistema financiero peruano.
          </p>
        </div>

        <div class="text-sm">
          <p class="font-semibold text-white">Equipo</p>
          <ul class="mt-3 space-y-1">
            <li v-for="member in team" :key="member">{{ member }}</li>
          </ul>
        </div>

        <div class="text-sm">
          <p class="font-semibold text-white">Legal</p>
          <ul class="mt-3 space-y-1">
            <li><a href="/privacidad" class="transition hover:text-white">Política de Privacidad</a></li>
            <li><a href="/terminos" class="transition hover:text-white">Términos de Servicio</a></li>
          </ul>
        </div>
      </div>

      <div class="mt-10 border-t border-white/10 pt-6 text-xs">
        Universidad Nacional de San Agustín · 2026 — Proyecto académico TuGasto
      </div>
    </div>
  </footer>
</template>
