<script setup lang="ts">
import type { Project } from '@/types/project'

defineProps<{
  project: Project
}>()
</script>

<template>
  <article class="project-card">
    <h3>
      {{ project.title }}
    </h3>

    <p>
      {{ project.description }}
    </p>

    <div class="project-card__technologies">
      <span v-for="technology in project.technologies" :key="technology">
        {{ technology }}
      </span>
    </div>

    <a v-if="project.link" :href="project.link"> View project </a>
  </article>
</template>
