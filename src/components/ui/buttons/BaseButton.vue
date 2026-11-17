
<script setup>
    defineProps({
    color: {
        type: String,
        default: 'primary',
    },
    size: {
        type: String,
        default: 'md',
    },
    loading: {
        type: Boolean,
        default: false,
    },
    disabled: {
        type: Boolean,
        default: false,
    },
    block: {
        type: Boolean,
        default: false,
    },
    type: {
        type: String,
        default: 'button',
    },
})

    const colors = {
    primary: 'bg-primary hover:bg-primary-hover',
    secondary: 'bg-secondary hover:bg-secondary-hover',
    success: 'bg-success hover:bg-green-700',
    danger: 'bg-danger hover:bg-red-700',
    }

    const sizes = {
    sm: 'px-3 py-2 text-sm',
    md: 'px-5 py-3 text-base',
    lg: 'px-6 py-4 text-lg',
    }
</script>

<template>
  <button
  :type="type"
  :disabled="disabled || loading"
  class="base-button"
  :class="[
    colors[color] || colors.primary,
    sizes[size] || sizes.md,
    block ? 'w-full' : 'w-auto',
    (disabled || loading) ? 'opacity-50 cursor-not-allowed' : 'cursor-pointer'
  ]"
  >
    <!-- Loading -->
    <span v-if="loading">
      Loading...
    </span>

    <!-- Normal Button Content -->
    <slot v-else />
  </button>
</template>

<style scoped>
@reference "@/assets/main.css";
.base-button {
  @apply rounded-lg font-semibold text-white transition duration-200;
}
</style>