<script setup>
import DownloadButtons from './DownloadButtons.vue'
</script>

<template>
  <section id="descargar" class="mx-auto max-w-4xl px-6 py-24 text-center">
    <h2 class="text-3xl font-extrabold text-navy sm:text-4xl">
      Pruébala ahora mismo
    </h2>
    <p class="mx-auto mt-4 max-w-xl text-navy-soft">
      Publicamos cada nueva versión para que la descargues e instales al
      instante, sin esperar aprobación de tienda.
    </p>
    <div class="mt-8 flex justify-center">
      <DownloadButtons />
    </div>
  </section>
</template>
