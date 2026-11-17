
<script setup>
defineProps({
  label: {
    type: String,
    default: '',
  },

  type: {
    type: String,
    default: 'text',
  },

  placeholder: {
    type: String,
    default: '',
  },

  disabled: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <div>
    <!-- Input Label -->
    <label
      v-if="label"
      class="block text-sm font-medium text-foreground mb-2"
    >
      {{ label }}
    </label>

    <!-- Input Field -->
    <input
      :type="type"
      :placeholder="placeholder"
      :disabled="disabled"
      class="w-full px-4 py-3 border border-border rounded-lg outline-none focus:ring-1 focus:ring-primary disabled:opacity-50 disabled:cursor-not-allowed"
    />
  </div>
</template>
