<script setup>
import ChatScreenMock from './mockups/ChatScreenMock.vue'
import DashboardScreenMock from './mockups/DashboardScreenMock.vue'
</script>

<template>
  <section class="mx-auto max-w-6xl px-6 py-20">
    <div class="mx-auto max-w-2xl text-center">
      <h2 class="text-3xl font-extrabold text-navy sm:text-4xl">Pantallas del MVP</h2>
      <p class="mt-3 text-navy-soft">
        Una experiencia simple: cuéntale tu gasto y mira cómo se ordena solo.
      </p>
    </div>

    <div class="mt-14 grid gap-16 sm:grid-cols-2">
      <div class="flex flex-col items-center gap-6">
        <ChatScreenMock />
        <p class="font-semibold text-navy">Sección de chat</p>
      </div>
      <div class="flex flex-col items-center gap-6">
        <DashboardScreenMock />
        <p class="font-semibold text-navy">Dashboard: gráficos dinámicos</p>
      </div>
    </div>
  </section>
</template>
