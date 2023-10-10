<template>
  <section
    class="ch-navbar fixed w-full bg-black text-white h-16 px-5 md:px-6 flex justify-between items-center"
  >
    <section class="flex-initial">
      <NuxtLink to="/">
        <img src="~/assets/CH Logo.svg" alt="Critical Hit Studio Logo" />
      </NuxtLink>
    </section>

    <section class="flex-initial uppercase">
      <NuxtLink
        to="/#ch-work"
        class="hidden sm:inline-block p-2 font-display font-bold"
      >
        Work
      </NuxtLink>
      <NuxtLink
        to="/#ch-services"
        class="hidden sm:inline-block p-2 font-display font-bold"
      >
        Services
      </NuxtLink>
      <NuxtLink
        to="/#ch-about-us"
        class="hidden sm:inline-block p-2 font-display font-bold"
      >
        About us
      </NuxtLink>
      <a
        href="mailto:criticalhit.creative.studio@gmail.com"
        class="inline-block bg-white text-black py-3 px-6 rounded-full font-display font-bold"
      >
        Let's talk
      </a>
    </section>
  </section>
</template>

<script>
export default {}
</script>
