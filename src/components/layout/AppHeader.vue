<script setup lang="ts">
import { ref, watch } from 'vue'
import { RouterLink, useRoute } from 'vue-router'

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

const route = useRoute()

const isMenuOpen = ref(false)

const toggleMenu = (): void => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = (): void => {
  isMenuOpen.value = false
}

watch(
  () => route.path,
  () => {
    closeMenu()
  },
)
</script>

<template>
  <header class="site-header">
    <div class="site-header__inner">
      <RouterLink class="site-header__brand" to="/" @click="closeMenu">
        <span>JLGB</span>
        Tech
      </RouterLink>

      <button
        class="site-header__toggle"
        :class="{
          'site-header__toggle--open': isMenuOpen,
        }"
        type="button"
        :aria-expanded="isMenuOpen"
        aria-controls="main-navigation"
        aria-label="Toggle navigation"
        @click="toggleMenu"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>

      <nav
        id="main-navigation"
        class="site-header__navigation"
        :class="{
          'site-header__navigation--open': isMenuOpen,
        }"
      >
        <RouterLink
          v-for="item in navigation"
          :key="item.to"
          :to="item.to"
          class="site-header__link"
        >
          {{ item.label }}
        </RouterLink>
      </nav>
    </div>
  </header>
</template>
