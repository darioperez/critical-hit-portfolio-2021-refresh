<template>
  <section>
    <ChNavbar class="z-20" />

    <ChProjectHeader
      :title="project.title"
      :subtitle="project.subtitle"
      :hero-url="project.heroImage"
    />

    <!-- <ChProjectLogos class="max-w-4xl mx-auto py-20" /> -->

    <section class="max-w-4xl mx-auto text-xl">
      <NuxtContent :document="project" />
    </section>

    <!-- TODO: ❌ Remove ChProjectDescription component and reimplement only with NuxtContent -->
    <!-- <ChProjectDescription /> -->

    <ChProjectNextProject
      class="block max-w-4xl mx-auto mt-40 mb-20"
      :project="nextProject"
    />

    <ChFooter class="mt-20" />
  </section>
</template>

<script>
import ChNavbar from '@/components/ch-components/ChNavbar.vue'
import ChFooter from '@/components/ch-components/ChFooter.vue'
import ChProjectHeader from '@/components/ch-components/projects/ChProjectHeader.vue'
import ChProjectNextProject from '@/components/ch-components/projects/ChProjectNextProject.vue'

export default {
  components: {
    ChNavbar,
    ChFooter,
    ChProjectHeader,
    ChProjectNextProject,
  },
  async asyncData({ $content, params }) {
    const projects = await $content('projects').fetch()

    let project = projects.findIndex(
      (project) => project.projectId === params.id
    )

    let nextProject = project + 1 >= projects.length ? 0 : project + 1

    project = projects[project]
    nextProject = projects[nextProject]

    return {
      project,
      nextProject,
    }
  },
}
</script>

<style lang="pcss">
.nuxt-content .ch-project__logos {
  @apply flex;
  @apply items-center;
  @apply justify-center;
  @apply flex-col;
  @apply md:flex-row;
  @apply my-20;
  @apply space-x-0;
  @apply md:space-x-12;
  @apply space-y-12;
  @apply md:space-y-0;
  @apply px-12;
  @apply md:px-0;
}

.nuxt-content .ch-project__intro {
  @apply md:pl-60;
  @apply mb-20;
  @apply px-5;
  @apply md:px-0;
}

.nuxt-content .ch-project__outcome {
  @apply px-5;
  @apply md:px-0;
}

.nuxt-content .ch-project__logos > img {
  @apply flex-initial;
}

.nuxt-content h2 {
  @apply mb-4 font-bold text-2xl;
}

.nuxt-content h3 {
  @apply mb-4 font-bold;
}

.nuxt-content p {
  @apply text-xl mb-4;
}

.nuxt-content p:last-child {
  @apply mb-0;
}

.nuxt-content .section {
  @apply mb-10;
}
</style>
