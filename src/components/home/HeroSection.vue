<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="hero">
    <div class="hero__content">
      <p class="hero__eyebrow">JLGB Tech</p>

      <h1>I build software, automate workflows and teach technology.</h1>

      <p class="hero__intro">
        Software Developer, DevOps learner and Technical Trainer focused on building reliable
        applications and sharing technical knowledge.
      </p>

      <div class="hero__actions">
        <RouterLink class="button button--primary" to="/projects"> View my projects </RouterLink>

        <RouterLink class="button button--secondary" to="/contact"> Contact me </RouterLink>
      </div>
    </div>

    <div class="hero__stack">
      <span>PHP</span>
      <span>Symfony</span>
      <span>Vue</span>
      <span>TypeScript</span>
      <span>Docker</span>
      <span>CI/CD</span>
    </div>
  </section>
</template>
