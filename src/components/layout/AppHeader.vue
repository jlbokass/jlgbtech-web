<script setup lang="ts">
import { RouterLink } from 'vue-router'

type NavItem = {
  label: string
  to: string
}

const navigation: NavItem[] = [
  {
    label: 'Home',
    to: '/',
  },
  {
    label: 'Projects',
    to: '/projects',
  },
  {
    label: 'Services',
    to: '/services',
  },
  {
    label: 'Training',
    to: '/training',
  },
  {
    label: 'About',
    to: '/about',
  },
  {
    label: 'Contact',
    to: '/contact',
  },
]
</script>

<template>
  <header>
    <RouterLink to="/"> JLGB Tech </RouterLink>

    <nav>
      <RouterLink v-for="item in navigation" :key="item.to" :to="item.to">
        {{ item.label }}
      </RouterLink>
    </nav>
  </header>
</template>
