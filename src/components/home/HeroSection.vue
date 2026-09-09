<script setup lang="ts">
import BaseButton from '@/components/ui/BaseButton.vue'
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
        <BaseButton to="/projects"> View my projects </BaseButton>

        <BaseButton to="/contact" variant="secondary"> Contact me </BaseButton>
      </div>
    </div>

    <div class="hero__stack">
      <span>PHP</span>
      <span>Symfony</span>
      <span>WP / WooCommerce</span>
      <span>Vue</span>
      <span>TypeScript</span>
      <span>Docker</span>
      <span>CI/CD</span>
    </div>
  </section>
</template>
