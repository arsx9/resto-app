
<template>
  <div class="auth-card">
    <div class="auth-header">
      <slot name="header" />
    </div>

    <div class="auth-body">
      <slot />
    </div>

    <div class="auth-footer">
      <slot name="footer" />
    </div>
  </div>
</template>

<style scoped>
@reference "@/assets/main.css";

.auth-card {
  @apply w-full max-w-md bg-surface rounded-2xl shadow-lg border border-border p-8;
}

.auth-header {
  @apply text-center mb-6;
}

.auth-body {
  @apply w-full;
}

.auth-footer {
  @apply mt-6 text-center text-sm text-text-secondary;
}
</style>