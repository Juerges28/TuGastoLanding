<script setup>
import PhoneFrame from './PhoneFrame.vue'
import Icon from '../icons/Icon.vue'
</script>

<template>
  <PhoneFrame>
    <div class="flex h-full flex-col px-4 pb-3 pt-1">
      <p class="mb-3 text-sm font-bold text-navy">Mi Dashboard</p>

      <div class="mb-3 flex rounded-full bg-paper-soft p-1 text-[10px] font-semibold">
        <span class="flex-1 rounded-full py-1 text-center text-navy-soft">Semana</span>
        <span class="flex-1 rounded-full bg-brand py-1 text-center text-white">Mes</span>
      </div>

      <div class="mb-3 rounded-2xl bg-white p-3 shadow-sm">
        <p class="text-[9px] font-semibold uppercase tracking-wide text-navy-soft/70">Total gastado (este mes)</p>
        <p class="text-xl font-extrabold text-navy">S/ 81.30</p>
        <p class="mt-1 flex items-center gap-1 text-[9px] text-navy-soft/70">
          Actualizado hace 5 min
          <span class="ml-1 inline-flex items-center gap-0.5 rounded-full bg-brand-light/15 px-1.5 py-0.5 font-semibold text-brand-dark">
            <Icon name="arrow-down" class="h-2.5 w-2.5" />8% vs mes anterior
          </span>
        </p>
      </div>

      <div class="flex-1 rounded-2xl bg-white p-3 shadow-sm">
        <p class="mb-2 text-[9px] font-semibold uppercase tracking-wide text-navy-soft/70">Distribución de gastos</p>
        <div class="flex justify-center py-1">
          <div
            class="relative flex h-24 w-24 items-center justify-center rounded-full"
            style="background: conic-gradient(#12a883 0deg 130deg, #f59e0b 130deg 165deg, #d9d2d6 165deg 360deg);"
          >
            <div class="flex h-14 w-14 flex-col items-center justify-center rounded-full bg-white text-center">
              <span class="text-[10px] font-bold text-navy">S/ 81.30</span>
              <span class="text-[7px] text-navy-soft/70">total</span>
            </div>
          </div>
        </div>
        <div class="mt-2 flex justify-center gap-3 text-[8px] text-navy-soft">
          <span class="flex items-center gap-1"><span class="h-1.5 w-1.5 rounded-full bg-[#d9d2d6]"></span>Otros</span>
          <span class="flex items-center gap-1"><span class="h-1.5 w-1.5 rounded-full bg-[#12a883]"></span>Alimentación</span>
          <span class="flex items-center gap-1"><span class="h-1.5 w-1.5 rounded-full bg-[#f59e0b]"></span>Transporte</span>
        </div>
      </div>
    </div>
  </PhoneFrame>
</template>
