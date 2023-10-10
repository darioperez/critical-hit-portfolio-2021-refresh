<template>
  <NuxtLink :to="`/projects/${projectId}`" class="ch-work-item block">
    <article class="text-xl">
      <img class="mb-4 w-full" :src="src" alt="" />

      <h1 class="font-bold mb-2">{{ title }}</h1>

      <section>
        <p>{{ description }}.</p>
      </section>
      <p class="mt-2 text-sm text-gray-500">{{ tags }}</p>
    </article>
  </NuxtLink>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    tags: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    projectId: {
      type: String,
      required: true,
    },
  },
}
</script>
