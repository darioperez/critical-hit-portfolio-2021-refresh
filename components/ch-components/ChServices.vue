<template>
  <section class="ch-section--services py-40 px-5 md:px-12">
    <div class="max-w-4xl mx-auto">
      <h2 class="uppercase font-black mb-6">Skills — Our services</h2>

      <p class="font-display text-5xl mb-6">Get a buff in your goals.</p>

      <div class="flex flex-col md:flex-row mb-6 space-y-6">
        <ChServiceItem
          class="flex-initial md:w-1/3 mr-6"
          src="web"
          label="Web"
        />
        <ChServiceItem
          class="flex-initial md:w-1/3 mr-6"
          src="mobile"
          label="Mobile"
        />
        <ChServiceItem
          class="flex-initial md:w-1/3"
          src="concept & prototyping"
          label="Concept & Prototyping"
        />
      </div>

      <div class="flex flex-col md:flex-row mb-6 space-y-6">
        <ChServiceItem
          class="flex-initial md:w-1/3 mr-6"
          src="strategy & branding"
          label="Strategy & Branding"
        />
        <ChServiceItem
          class="flex-initial md:w-1/3 mr-6"
          src="marketing"
          label="Marketing"
        />
        <ChServiceItem
          class="flex-initial md:w-1/3"
          src="product consulting"
          label="Product Consulting"
        />
      </div>

      <div class="text-xl max-w-xl">
        <p class="mb-6">
          With care to detail and love for excellence our team built beautiful
          and highly efficient web experiences and brands.
        </p>
        <p class="mb-6">
          Whether creating something new or improving something existing, we
          help brands to reach their customers and craft digital products.
        </p>
        <p class="mb-6">
          We also provide in-house team improvement and level up through
          orientation and consultancy.
        </p>
        <p class="">
          Our party is formed by specialists armed with modern technologies,
          ready to face any challenge and hit the best results. We explore,
          research and plan, design and develop, test and deliver lasting and
          reliable solutions.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import ChServiceItem from '@/components/ch-components/ChServiceItem.vue'
export default {
  components: {
    ChServiceItem,
  },
}
</script>

<style lang="pcss">
.ch-section--services {
  background: #efebec;
}
</style>
