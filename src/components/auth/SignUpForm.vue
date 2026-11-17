
<script setup>
import AuthCard from '@/components/auth/AuthCard.vue'
import BaseInput from '@/components/ui/inputs/Input.vue'
import BaseButton from '@/components/ui/buttons/BaseButton.vue'
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
      <BaseInput
        label="Full Name"
        placeholder="Enter your full name"
      />

      <BaseInput
        label="Email Address"
        type="email"
        placeholder="Enter your email"
      />

      <BaseInput
        label="Password"
        type="password"
        placeholder="Create a password"
      />
      <BaseButton block>
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
