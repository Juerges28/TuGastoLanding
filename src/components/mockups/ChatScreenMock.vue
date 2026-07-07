<script setup>
import PhoneFrame from './PhoneFrame.vue'
import Icon from '../icons/Icon.vue'
</script>

<template>
  <PhoneFrame>
    <div class="flex h-full flex-col px-4 pb-3 pt-2">
      <p class="mb-3 text-center text-xs font-semibold text-navy-soft">Asistente TuGasto</p>

      <div class="flex flex-1 flex-col gap-2 overflow-hidden">
        <div class="flex justify-end">
          <span class="rounded-2xl rounded-tr-sm bg-brand px-3 py-1.5 text-xs font-medium text-white">pan 2 so</span>
        </div>
        <div class="flex justify-start">
          <div class="max-w-[85%] rounded-2xl rounded-tl-sm bg-white px-3 py-2 text-[11px] leading-relaxed text-navy shadow-sm">
            <p class="flex items-center gap-1 font-semibold text-brand">
              <Icon name="check" class="h-3 w-3" />Registrado
            </p>
            <p>Detalle: pan 2 so</p>
            <p>Categoría: Alimentación</p>
            <p>Monto: S/ 2.0</p>
            <span class="mt-1 inline-block rounded-full bg-paper-soft px-2 py-0.5 text-[10px] font-medium text-brand">Alimentación</span>
          </div>
        </div>

        <div class="flex justify-end">
          <span class="rounded-2xl rounded-tr-sm bg-brand px-3 py-1.5 text-xs font-medium text-white">pasaje 1.30</span>
        </div>
        <div class="flex justify-start">
          <div class="max-w-[85%] rounded-2xl rounded-tl-sm bg-white px-3 py-2 text-[11px] leading-relaxed text-navy shadow-sm">
            <p class="flex items-center gap-1 font-semibold text-brand">
              <Icon name="check" class="h-3 w-3" />Registrado
            </p>
            <p>Detalle: pasaje 1.30</p>
            <p>Categoría: Transporte</p>
            <p>Monto: S/ 1.3</p>
            <span class="mt-1 inline-block rounded-full bg-paper-soft px-2 py-0.5 text-[10px] font-medium text-brand">Transporte</span>
          </div>
        </div>
      </div>

      <div class="mt-3 flex items-center gap-2 rounded-full border border-black/10 bg-white px-3 py-2">
        <span class="flex-1 truncate text-[11px] text-navy-soft/70">Escribe tu gasto... ej: café 8 S/</span>
        <span class="flex h-6 w-6 items-center justify-center rounded-full bg-brand text-white">
          <Icon name="send" class="h-3 w-3" />
        </span>
      </div>
    </div>
  </PhoneFrame>
</template>
