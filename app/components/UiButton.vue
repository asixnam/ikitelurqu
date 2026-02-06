<script setup lang="ts">
defineProps<{
  variant?: 'primary' | 'outline' | 'text'
  size?: 'sm' | 'md' | 'lg'
  block?: boolean
}>()
</script>

<template>
  <button 
    class="ui-button" 
    :class="[
      `variant-${variant || 'primary'}`,
      `size-${size || 'md'}`,
      { 'is-block': block }
    ]"
  >
    <slot />
  </button>
</template>

<style scoped>
.ui-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
  border-radius: 50px; /* Pill shape */
  cursor: pointer;
  transition: all 0.2s ease;
  border: 2px solid transparent;
  outline: none;
}

.ui-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(245, 158, 11, 0.3);
}

.ui-button:active {
  transform: translateY(0);
}

/* Variants */
.variant-primary {
  background-color: var(--color-primary);
  color: white;
}
.variant-primary:hover {
  background-color: var(--color-primary-dark);
}

.variant-outline {
  background-color: transparent;
  border-color: var(--color-primary);
  color: var(--color-primary);
}
.variant-outline:hover {
  background-color: var(--color-primary);
  color: white;
}

.variant-text {
  background-color: transparent;
  color: var(--color-text-main);
  padding-left: 0;
  padding-right: 0;
}
.variant-text:hover {
  color: var(--color-primary);
  background-color: transparent;
  box-shadow: none;
  transform: none;
}

/* Sizes */
.size-sm {
  padding: 8px 16px;
  font-size: 0.875rem;
}
.size-md {
  padding: 12px 24px;
  font-size: 1rem;
}
.size-lg {
  padding: 16px 32px;
  font-size: 1.125rem;
}

.is-block {
  width: 100%;
}
</style>
