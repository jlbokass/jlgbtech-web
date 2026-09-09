<script setup lang="ts">
import ProjectCard from '@/components/home/ProjectCard.vue'

import type { Project } from '@/types/project'

const projects: Project[] = [
  {
    id: 1,
    title: 'Refuge de l’Hôte',
    description: 'Booking platform with online payments and multilingual support.',
    technologies: ['Symfony', 'Stripe', 'MySQL', 'Bootstrap'],
  },

  {
    id: 2,
    title: 'CHAPOBA',
    description: 'Web platform for managing activities and registrations for a dance association.',
    technologies: ['Symfony', 'Vue', 'Docker'],
  },

  {
    id: 3,
    title: 'JLGB Coach',
    description: 'Student coaching platform with dashboards, sessions and learning resources.',
    technologies: ['Vue', 'TypeScript', 'Symfony', 'REST API'],
  },
]
</script>

<template>
  <section class="section">
    <div class="section__header">
      <p class="section__eyebrow">Selected work</p>

      <h2>Projects built around real needs.</h2>
    </div>

    <div class="projects-grid">
      <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
    </div>
  </section>
</template>
