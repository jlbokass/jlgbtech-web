<script setup lang="ts">
import { RouterLink } from 'vue-router'

type ButtonVariant = 'primary' | 'secondary'

withDefaults(
  defineProps<{
    to: string
    variant?: ButtonVariant
  }>(),
  {
    variant: 'primary',
  },
)
</script>

<template>
  <RouterLink :to="to" class="button" :class="`button--${variant}`">
    <slot />
  </RouterLink>
</template>
