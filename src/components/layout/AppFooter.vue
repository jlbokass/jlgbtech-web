<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="site-footer">
    <div class="site-footer__inner">
      <div>
        <strong>JLGB Tech</strong>

        <p>Software Development · DevOps · Technical Training</p>
      </div>

      <p>© {{ currentYear }} JLGB Tech</p>
    </div>
  </footer>
</template>
