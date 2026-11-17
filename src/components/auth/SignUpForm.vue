
<script setup>
import AuthCard from './AuthCard.vue'
import BaseButton from '../common/BaseButton.vue'
</script>

<template>
  <AuthCard>
    <template #header>
      <h1 class="text-2xl font-bold text-primary">
        Create Account
      </h1>

      <p class="text-text-secondary mt-2 text-sm">
        Create your account to get started.
      </p>
    </template>

    <form class="space-y-4" @submit.prevent>
      <div>
        <label class="block text-sm font-medium text-foreground mb-2">
          Full Name
        </label>

        <input
          type="text"
          placeholder="Enter your full name"
          class="w-full px-4 py-3 border border-border rounded-lg outline-none focus:border-primary"
        />
      </div>

      <div>
        <label class="block text-sm font-medium text-foreground mb-2">
          Email Address
        </label>

        <input
          type="email"
          placeholder="Enter your email"
          class="w-full px-4 py-3 border border-border rounded-lg outline-none focus:border-primary"
        />
      </div>

      <div>
        <label class="block text-sm font-medium text-foreground mb-2">
          Password
        </label>

        <input
          type="password"
          placeholder="Create a password"
          class="w-full px-4 py-3 border border-border rounded-lg outline-none focus:border-primary"
        />
      </div>

      <BaseButton color="primary">
        Create Account
      </BaseButton>
    </form>

    <template #footer>
      Already have an account?
      <a href="#" class="text-primary font-semibold hover:underline">
        Sign In
      </a>
    </template>
  </AuthCard>
</template>
