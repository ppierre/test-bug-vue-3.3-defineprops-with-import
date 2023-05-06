<script setup lang="ts">
// Bug
import type { MaisonResponse } from '@/pocketbase-types'
// Work with extra import `MaisonRecord`
// import type { MaisonResponse, MaisonRecord } from '@/pocketbase-types'
defineProps<MaisonResponse>()
</script>
<template>
  <p>
    {{ nomMaison }}
  </p>
</template>
