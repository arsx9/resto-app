
<script setup>
defineProps({
  color: {
    type: String,
    default: 'primary',
  },
})

const colors = {
  primary: 'bg-primary hover:bg-primary-hover',
  secondary: 'bg-secondary hover:bg-secondary-hover',
  success: 'bg-success hover:bg-green-700',
  danger: 'bg-danger hover:bg-red-700',
}
</script>

<template>
  <button
    type="button"
    class="base-button"
    :class="colors[color] || colors.primary"
  >
    <slot />
  </button>
</template>

<style scoped>
@reference "../../assets/main.css";

.base-button {
  @apply w-full px-5 py-3 rounded-lg font-semibold text-white
         transition duration-200 cursor-pointer;
}
</style>