<script setup>
const partners = [
  { name: 'Supabase', text: 'Backend as a Service · PostgreSQL' },
  { name: 'Groq', text: 'Inferencia LPU ultrarrápida' },
  { name: 'Google', text: 'OAuth 2.0 y API de Gmail' },
]
</script>

<template>
  <section class="border-y border-black/5 bg-white py-14">
    <div class="mx-auto max-w-6xl px-6">
      <p class="text-center text-xs font-semibold uppercase tracking-widest text-navy-soft/60">
        Construido con tecnología de nivel mundial
      </p>
      <div class="mt-8 grid gap-8 sm:grid-cols-3">
        <div v-for="p in partners" :key="p.name" class="text-center">
          <p class="font-display text-xl font-bold text-navy">{{ p.name }}</p>
          <p class="mt-1 text-sm text-navy-soft">{{ p.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
