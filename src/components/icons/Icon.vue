<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <svg
    viewBox="0 0 24 24"
    fill="none"
    stroke="currentColor"
    stroke-width="1.75"
    stroke-linecap="round"
    stroke-linejoin="round"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path v-if="name === 'chat'" d="M4 5h16a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1h-9l-4.5 3.5V17H4a1 1 0 0 1-1-1V6a1 1 0 0 1 1-1z" />

    <g v-else-if="name === 'sparkles'" fill="currentColor" stroke="none">
      <path d="M12 3l1.3 3.7L17 8l-3.7 1.3L12 13l-1.3-3.7L7 8l3.7-1.3L12 3z" />
      <path d="M18.5 14l.6 1.7 1.7.6-1.7.6-.6 1.7-.6-1.7-1.7-.6 1.7-.6.6-1.7z" />
    </g>

    <template v-else-if="name === 'chart-bar'">
      <path d="M5 21V13M11 21V7M17 21v-9" />
      <path d="M3 21h18" />
    </template>

    <template v-else-if="name === 'mail'">
      <path d="M4 6h16a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1V7a1 1 0 0 1 1-1z" />
      <path d="M3.5 7.2 12 13l8.5-5.8" />
    </template>

    <template v-else-if="name === 'shield'">
      <path d="M12 3l7 3v6c0 4.5-3 8-7 9-4-1-7-4.5-7-9V6l7-3z" />
      <path d="M9 12l2 2 4-4" />
    </template>

    <path v-else-if="name === 'bolt'" d="M13 2 4 14h6l-1 8 9-12h-6l1-8z" fill="currentColor" stroke="none" />

    <template v-else-if="name === 'bell'">
      <path d="M6 10a6 6 0 0 1 12 0c0 4 1.5 6 2 7H4c.5-1 2-3 2-7z" />
      <path d="M9.5 19a2.5 2.5 0 0 0 5 0" />
    </template>

    <path v-else-if="name === 'check'" d="M4 12.5l5 5L20 7" />

    <template v-else-if="name === 'menu'">
      <path d="M4 6h16" />
      <path d="M4 12h16" />
      <path d="M4 18h16" />
    </template>

    <template v-else-if="name === 'close'">
      <path d="M6 6l12 12" />
      <path d="M18 6L6 18" />
    </template>

    <path v-else-if="name === 'send'" d="M4 20l17-8L4 4v6.5L15 12 4 13.5V20z" fill="currentColor" stroke="none" />

    <template v-else-if="name === 'alert-triangle'">
      <path d="M12 4 2 20h20L12 4z" />
      <path d="M12 10v5" />
      <path d="M12 17.5h.01" />
    </template>

    <template v-else-if="name === 'lightbulb'">
      <path d="M9 18h6M10 21h4" />
      <path d="M12 3a6 6 0 0 0-3.5 10.9c.5.4.8 1 .8 1.6h5.4c0-.6.3-1.2.8-1.6A6 6 0 0 0 12 3z" />
    </template>

    <template v-else-if="name === 'arrow-up'">
      <path d="M12 19V5" />
      <path d="M6 11l6-6 6 6" />
    </template>

    <template v-else-if="name === 'arrow-down'">
      <path d="M12 5v14" />
      <path d="M18 13l-6 6-6-6" />
    </template>

    <template v-else-if="name === 'briefcase'">
      <path d="M4 8h16a1 1 0 0 1 1 1v9a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1V9a1 1 0 0 1 1-1z" />
      <path d="M9 8V6a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2v2" />
    </template>

    <template v-else-if="name === 'graduation-cap'">
      <path d="M2 9l10-5 10 5-10 5-10-5z" />
      <path d="M6 11.5v4c0 1.5 3 3 6 3s6-1.5 6-3v-4" />
      <path d="M22 9v6" />
    </template>

    <template v-else-if="name === 'smartphone'">
      <path d="M7 2h10a1 1 0 0 1 1 1v18a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V3a1 1 0 0 1 1-1z" />
      <path d="M11 18h2" />
    </template>

    <template v-else-if="name === 'wifi'">
      <path d="M2 8.5a15 15 0 0 1 20 0" />
      <path d="M5.5 12a10 10 0 0 1 13 0" />
      <path d="M9 15.5a5 5 0 0 1 6 0" />
      <path d="M12 19h.01" />
    </template>

    <template v-else-if="name === 'battery'">
      <rect x="2" y="7.5" width="18" height="9" rx="2" />
      <path d="M22 10.5v3" />
      <rect x="4" y="9.5" width="12" height="5" rx="1" fill="currentColor" stroke="none" />
    </template>

    <template v-else-if="name === 'download'">
      <path d="M12 3v12" />
      <path d="M7 10l5 5 5-5" />
      <path d="M4 21h16" />
    </template>

    <!-- GitHub logo -->
    <path
      v-else-if="name === 'github'"
      fill="currentColor"
      stroke="none"
      d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.341-3.369-1.341-.454-1.154-1.11-1.462-1.11-1.462-.908-.62.069-.608.069-.608 1.003.07 1.532 1.03 1.532 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0 1 12 6.836a9.59 9.59 0 0 1 2.504.337c1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.579.688.481C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"
    />

    <!-- APKPure – simplified "A" shield mark -->
    <g v-else-if="name === 'apkpure'" fill="currentColor" stroke="none">
      <path d="M12 2L3 6.5v5C3 16.36 6.96 21.24 12 22c5.04-.76 9-5.64 9-10.5v-5L12 2z" opacity=".2"/>
      <path d="M12 2L3 6.5v5C3 16.36 6.96 21.24 12 22c5.04-.76 9-5.64 9-10.5v-5L12 2zm0 2.18l7 3.82v4.5c0 3.87-3.13 7.8-7 8.48-3.87-.68-7-4.61-7-8.48V8l7-3.82z"/>
      <path d="M9 16l1.5-3.5h3L15 16h-1.5l-.5-1.2h-2L10.5 16H9zm2.3-2.4h1.4l-.7-1.8-.7 1.8z"/>
    </g>
  </svg>
</template>
