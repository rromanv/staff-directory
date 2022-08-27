<script setup>
import { faker } from '@faker-js/faker'

const firstName = faker.name.firstName()
const lastName = faker.name.lastName()
const fullName = `${firstName} ${lastName}`
</script>

<template>
  <figure class="card">
    <img class="profile" :src="faker.image.avatar()" alt="avatar" />
    <div class="card-text">
      <blockquote>
        <p class="quote">"{{ faker.lorem.paragraph() }}"</p>
      </blockquote>
      <figcaption class="details">
        <div class="name">{{ fullName }}</div>
        <div class="job">
          {{ faker.name.jobTitle() }}, {{ faker.name.jobArea() }}
        </div>
        <div class="email">
          {{ faker.internet.exampleEmail(firstName, lastName) }}
        </div>
      </figcaption>
    </div>
  </figure>
</template>

<style lang="postcss" scoped>
.card {
  @apply bg-slate-100 rounded-xl p-8 shadow-md overflow-hidden;
  .profile {
    @apply rounded-full mx-auto object-contain;
  }
  &-text {
    @apply pt-6 text-center gap-4 flex flex-col;
    .quote {
      @apply text-lg font-medium text-slate-600;
    }
    .details {
      @apply font-medium flex flex-col gap-4 mt-auto;
      .name {
        @apply text-yellow-700 font-thin text-3xl;
      }
      .job {
        @apply text-slate-700 font-bold;
      }
      .email {
        @apply text-slate-700 text-xs;
      }
    }
  }
}
</style>
