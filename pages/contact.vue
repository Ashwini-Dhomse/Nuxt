<script setup lang="ts">
import type { FormError, FormSubmitEvent } from '#ui/types'

const state = reactive({
  email: undefined,
  query: undefined,
  firstname: undefined,
  lastname: undefined
})

const validate = (state: any): FormError[] => {
  const errors = []
  if (!state.firstname) errors.push({ path: 'firstname', message: 'Required' })
  if (!state.lastname) errors.push({ path: 'lastname', message: 'Required' })
  if (!state.email) errors.push({ path: 'email', message: 'Required' })
  if (!state.query) errors.push({ path: 'query', message: 'Required' })
  return errors
}

async function onSubmit (event: FormSubmitEvent<any>) {
  // Do something with data
  console.log(event.data)
}
</script>

<template>
    <div class="flex flex-col items-center">
    <h1>Contact Form</h1>
   
  <UForm :validate="validate" :state="state" class="space-y-4" @submit="onSubmit">
   <UFormGroup label="First Name" name="firstname">
      <UInput v-model="state.firstname" />
    </UFormGroup>

    <UFormGroup label="Last Name" name="lastname">
      <UInput v-model="state.lastname" />
    </UFormGroup>

    <UFormGroup label="Email" name="email">
      <UInput v-model="state.email" />
    </UFormGroup>

    <UFormGroup label="Query" name="query">
      <UTextarea v-model="state.query" />
    </UFormGroup>

    <UButton type="submit">
      Submit
    </UButton>
  </UForm>
</div>
</template>