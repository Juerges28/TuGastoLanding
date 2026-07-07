<script setup>
import Icon from './icons/Icon.vue'

const features = [
  {
    icon: 'chat',
    title: 'Chat conversacional (Zero-UI)',
    text: 'Nada de menús ni formularios: registra un gasto igual que le escribirías a un amigo.',
  },
  {
    icon: 'mail',
    title: 'Detección automática de Yape/Plin',
    text: 'Nos conectamos de forma segura a tu Gmail para leer confirmaciones de pago y registrarlas solas.',
  },
  {
    icon: 'chart-bar',
    title: 'Dashboard con gráficos dinámicos',
    text: 'Distribución de gastos por categoría, comparativas semanales y mensuales, todo en un vistazo.',
  },
  {
    icon: 'shield',
    title: 'Tus datos, protegidos',
    text: 'Row Level Security en Supabase asegura que solo tú puedas ver y acceder a tu información financiera.',
  },
  {
    icon: 'bolt',
    title: 'IA ultrarrápida con Groq',
    text: 'Procesamiento de lenguaje natural a latencia mínima, entendiendo jerga peruana sin demoras.',
  },
  {
    icon: 'bell',
    title: 'Alertas predictivas (Pro)',
    text: 'Proyecciones de fin de mes y avisos antes de que tu presupuesto se salga de control.',
  },
]
</script>

<template>
  <section id="funciones" class="bg-paper-soft/60 py-20">
    <div class="mx-auto max-w-6xl px-6">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-extrabold text-navy sm:text-4xl">Todo lo que necesitas, sin esfuerzo</h2>
        <p class="mt-3 text-navy-soft">
          Diseñado para adultos activos y universitarios que mueven microgastos todos los días.
        </p>
      </div>

      <div class="mt-14 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
        <div
          v-for="f in features"
          :key="f.title"
          class="rounded-2xl border border-black/5 bg-white p-6 transition hover:-translate-y-1 hover:shadow-md"
        >
          <span class="flex h-11 w-11 items-center justify-center rounded-xl bg-paper-soft text-brand">
            <Icon :name="f.icon" class="h-5 w-5" />
          </span>
          <h3 class="mt-4 font-bold text-navy">{{ f.title }}</h3>
          <p class="mt-2 text-sm leading-relaxed text-navy-soft">{{ f.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
