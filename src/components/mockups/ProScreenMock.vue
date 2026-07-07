<script setup>
import PhoneFrame from './PhoneFrame.vue'
import Icon from '../icons/Icon.vue'
</script>

<template>
  <PhoneFrame dark>
    <div class="flex h-full flex-col gap-2.5 px-4 pb-3 pt-1">
      <p class="text-sm font-bold text-white">Análisis Pro</p>

      <div class="rounded-2xl bg-navy-card p-3">
        <p class="text-[8px] font-semibold uppercase tracking-wide text-white/50">Pronóstico de julio</p>
        <div class="mt-1 flex justify-between">
          <div>
            <p class="text-[9px] text-white/60">Proyección a fin de mes</p>
            <p class="text-base font-bold text-white">S/ 348.43</p>
            <span class="flex items-center gap-0.5 text-[8px] font-semibold text-red-400">
              <Icon name="arrow-up" class="h-2.5 w-2.5" />5% vs mes ant.
            </span>
          </div>
          <div class="text-right">
            <p class="text-[9px] text-white/60">Saldo estimado</p>
            <p class="text-base font-bold text-white">S/ 2651.57</p>
            <span class="text-[8px] font-semibold text-brand-light">Dentro del plan</span>
          </div>
        </div>
      </div>

      <div class="rounded-2xl bg-navy-card p-3">
        <p class="text-[10px] font-semibold text-white">Progreso de Meta: Fondo de Emergencia</p>
        <p class="mt-0.5 text-[8px] text-white/50">Has ahorrado S/ 1500 de S/ 5000</p>
        <div class="mt-1.5 h-1.5 w-full overflow-hidden rounded-full bg-white/10">
          <div class="h-full w-[30%] rounded-full bg-brand-light"></div>
        </div>
      </div>

      <div class="flex-1 space-y-2 overflow-hidden rounded-2xl bg-navy-card p-3">
        <p class="flex items-center gap-1 text-[10px] font-semibold text-white">
          <Icon name="sparkles" class="h-3 w-3 text-brand-light" />Observaciones de la IA
        </p>
        <div class="rounded-xl bg-navy-card-2 p-2">
          <p class="flex items-center gap-1 text-[9px] font-semibold text-amber-400">
            <Icon name="alert-triangle" class="h-3 w-3" />Alerta
          </p>
          <p class="text-[8px] leading-snug text-white/60">Se sugiere revisar Alimentación, que representa el 44.5% del total.</p>
        </div>
        <div class="rounded-xl bg-navy-card-2 p-2">
          <p class="flex items-center gap-1 text-[9px] font-semibold text-brand-light">
            <Icon name="lightbulb" class="h-3 w-3" />Sugerencia
          </p>
          <p class="text-[8px] leading-snug text-white/60">Reestructura tu presupuesto mensual para optimizar tu liquidez.</p>
        </div>
      </div>
    </div>
  </PhoneFrame>
</template>
