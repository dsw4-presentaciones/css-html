<script setup>
import { ref } from 'vue'

const active = ref('html')
</script>

<template>
  <div>
    <div class="flex gap-2 mb-4">
      <button
        :class="active === 'html' ? 'bg-orange-500 text-white border-orange-500' : 'bg-orange-50 text-orange-700 border-orange-200'"
        class="rounded-md border px-4 py-1 font-semibold transition-colors"
        @click="active='html'"
      >
        HTML
      </button>
      <button
        :class="active === 'css' ? 'bg-blue-500 text-white border-blue-500' : 'bg-blue-50 text-blue-700 border-blue-200'"
        class="rounded-md border px-4 py-1 font-semibold transition-colors"
        @click="active='css'"
      >
        CSS
      </button>
      <button
        :class="active === 'result' ? 'bg-emerald-500 text-white border-emerald-500' : 'bg-emerald-50 text-emerald-700 border-emerald-200'"
        class="rounded-md border px-4 py-1 font-semibold transition-colors"
        @click="active='result'"
      >
        Result
      </button>
    </div>

    <div v-if="active==='html'">
      <slot name="html" />
    </div>

    <div v-if="active==='css'">
      <slot name="css" />
    </div>

    <div v-if="active==='result'">
      <slot name="result" />
    </div>
  </div>
</template>