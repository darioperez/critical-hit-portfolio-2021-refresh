<template>
  <section class="py-40 px-5 md:px-12">
    <div class="max-w-4xl mx-auto mb-40">
      <h2 class="uppercase font-black mb-6">Quests — My contributions</h2>

      <p class="font-display text-5xl mb-6">
        The people we help,<br />The friends we made.
      </p>

      <p class="text-xl max-w-xl mb-9">
        In my many advertures I have forged bonds of fate with unmatched allies.
        These are some of them.
      </p>

      <!-- Client's Logos -->
      <section
        class="flex items-center justify-between md:justify-start flex-wrap md:flex-nowrap md:space-x-12"
      >
        <!-- Plug Altermedia Logo -->
        <div class="flex-none w-1/5 md:flex-auto mb-6 md:mb-0">
          <img
            src="~/assets/logos/plugaltermedia-logo.png"
            alt=""
            class="max-h-32"
          />
        </div>

        <!-- The MLS Logo -->
        <div class="flex-none w-1/4 md:flex-auto mb-6 md:mb-0">
          <img src="~/assets/logos/the-mls-logo.png" alt="" class="max-h-32" />
        </div>

        <!-- Algo Que Dar Logo -->
        <div class="flex-none w-1/5 md:flex-auto mb-6 md:mb-0">
          <img src="~/assets/logos/aqd-logo.svg" alt="" class="max-h-40" />
        </div>

        <!-- Rhombus Logo -->
        <div class="flex-none w-5/12 md:flex-auto">
          <img src="~/assets/logos/rhombus-logo.png" alt="" class="max-h-24" />
        </div>

        <!-- Europe Shuttle Logo -->
        <div class="flex-none w-5/12 md:flex-auto">
          <img
            src="~/assets/logos/europe-shuttle-logo.png"
            alt=""
            class="max-h-28"
          />
        </div>
      </section>
      <!--/ Client's Logos -->
    </div>

    <div class="ch-work-list flex flex-wrap max-w-4xl mx-auto">
      <ChWorkItem
        v-for="project of projects"
        :key="project.projectId"
        :src="project.thumbnail"
        :title="project.title"
        :tags="project.tags"
        :description="project.short"
        :project-id="project.projectId"
        class="ch-work-item md:w-9/12 mb-20"
      />
    </div>

    <!-- TODO: Uncomment this link when there exists Work section -->
    <!-- <div class="text-center my-20">
      <NuxtLink
        to=""
        class="text-xl text-brand uppercase font-bold border-b-4 border-brand"
        >View more <span class="line-through">works</span> adventures</NuxtLink
      >
    </div> -->
  </section>
</template>

<script>
import ChWorkItem from '@/components/ch-components/ChWorkItem.vue'

export default {
  components: {
    ChWorkItem,
  },
  props: {
    projects: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="pcss">
@media (min-width: 768px) {
  .ch-work-item:nth-child(odd) {
    @apply mr-auto;
  }

  .ch-work-item:nth-child(even) {
    @apply ml-auto;
  }
}

.ch-work-item:last-child {
  margin-bottom: 0;
}
</style>
