<template>
  <article
    class="flex flex-col md:flex-row items-center space-x-0 md:space-x-6 space-y-12 md:space-y-0 px-5 md:px-0"
  >
    <NuxtLink
      :to="`/projects/${project.projectId}`"
      class="flex-auto w-full md:w-2/3 flex flex-col md:flex-row items-center space-x-0 md:space-x-6 space-y-6 md:space-y-0"
    >
      <img
        class="flex-auto w-full md:w-1/2"
        :src="project.thumbnailSm"
        alt=""
      />

      <section class="flex-auto w-full md:w-1/2 space-y-4">
        <h1 class="font-display font-bold text-2xl">{{ project.title }}</h1>
        <p class="text-xl">{{ project.short }}.</p>
        <p class="text-sm text-gray-500">{{ project.tags }}.</p>
        <NuxtLink
          :to="`/projects/${project.projectId}`"
          class="inline-block text-xl uppercase font-bold border-b-4 border-black"
          >View <span class="">Project</span> Quest</NuxtLink
        >
      </section>
    </NuxtLink>

    <section class="flex-auto w-full md:w-1/3 text-center">
      <p class="font-display text-4xl md:text-6xl mb-6">Ready to roll?</p>

      <a
        href="mailto:dddarioperezzz@gmail.com"
        class="inline-block bg-brand text-white py-3 px-6 rounded-full font-display font-bold text-xl"
      >
        Let's talk
      </a>
    </section>
  </article>
</template>

<script>
export default {
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
}
</script>
