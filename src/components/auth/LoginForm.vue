
<script setup>
import AuthCard from '@/components/auth/AuthCard.vue'
import BaseInput from '@/components/ui/inputs/Input.vue'
import BaseButton from '@/components/ui/buttons/BaseButton.vue'
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
      <BaseInput
        label="Email Address"
        type="email"
        placeholder="Enter your email"
      />

      <BaseInput
        label="Password"
        type="password"
        placeholder="Enter your password"
      />

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
