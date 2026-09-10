<script setup lang="ts">
type Expertise = {
  title: string
  description: string
  technologies: string[]
}

const expertises: Expertise[] = [
  {
    title: 'Software Development',
    description: 'Design and development of maintainable web applications and APIs.',
    technologies: ['PHP', 'Symfony', 'MySQL', 'REST API', 'WP'],
  },
  {
    title: 'DevOps & Cloud',
    description: 'Building reliable development and deployment workflows.',
    technologies: ['Docker', 'GitHub Actions', 'Linux', 'CI/CD'],
  },
  {
    title: 'Technical Training',
    description: 'Teaching programming and software development through practical projects.',
    technologies: ['PHP', 'Python', 'C#', 'Web Development'],
  },
]
</script>

<template>
  <section class="section">
    <div class="section__header">
      <p class="section__eyebrow">Expertise</p>

      <h2>Development, infrastructure and knowledge sharing.</h2>
    </div>

    <div class="expertise-grid">
      <article v-for="expertise in expertises" :key="expertise.title" class="expertise-card">
        <h3>
          {{ expertise.title }}
        </h3>

        <p>
          {{ expertise.description }}
        </p>

        <ul>
          <li v-for="technology in expertise.technologies" :key="technology">
            {{ technology }}
          </li>
        </ul>
      </article>
    </div>
  </section>
</template>
