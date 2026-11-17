
<script setup>
import AuthCard from '@/components/auth/AuthCard.vue'
import BaseButton from '@/components/common/Buttons/BaseButton.vue'
</script>

<template>
  <AuthCard>
    <template #header>
      <h1 class="text-2xl font-bold text-primary">
        Welcome Back
      </h1>

      <p class="text-text-secondary mt-2 text-sm">
        Sign in to continue to your account.
      </p>
    </template>

    <form class="space-y-5" @submit.prevent>
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
          placeholder="Enter your password"
          class="w-full px-4 py-3 border border-border rounded-lg outline-none focus:border-primary"
        />
      </div>

      <div class="flex justify-end">
        <a href="#" class="text-sm text-primary hover:underline">
          Forgot password?
        </a>
      </div>

      <BaseButton block>
        Sign In
      </BaseButton>
    </form>

    <template #footer>
      Don't have an account?
      <a href="#" class="text-primary font-semibold hover:underline">
        Create account
      </a>
    </template>
  </AuthCard>
</template>
