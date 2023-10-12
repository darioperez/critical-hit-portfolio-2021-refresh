<template>
  <section class="ch-page ch-page--home">
    <ChNavbar />

    <ChHeader />

    <ChSubHeader />

    <ChWork id="ch-work" :projects="projects" />

    <ChServices id="ch-services" class="pb-0" />

    <ChWhyUs id="ch-about-us" />

    <ChContactUs />

    <ChFooter />
  </section>
</template>

<script>
import ChNavbar from '@/components/ch-components/ChNavbar.vue'
import ChHeader from '@/components/ch-components/ChHeader.vue'
import ChSubHeader from '@/components/ch-components/ChSubHeader.vue'
import ChWork from '@/components/ch-components/ChWork.vue'
import ChServices from '@/components/ch-components/ChServices.vue'
import ChWhyUs from '@/components/ch-components/ChWhyUs.vue'
import ChContactUs from '@/components/ch-components/ChContactUs.vue'
import ChFooter from '@/components/ch-components/ChFooter.vue'

export default {
  components: {
    ChNavbar,
    ChHeader,
    ChSubHeader,
    ChWork,
    ChServices,
    ChWhyUs,
    ChContactUs,
    ChFooter,
  },
  async asyncData({ $content }) {
    const projects = await $content('projects').fetch()

    return {
      projects,
    }
  },
  created() {},
}
</script>
