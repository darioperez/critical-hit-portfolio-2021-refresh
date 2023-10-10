<template>
  <section
    class="ch-project__header relative bg-black"
    :style="`background-image: url('${heroUrl}')`"
  >
    <div
      class="max-w-4xl absolute top-0 right-0 bottom-0 left-0 mx-auto flex justify-center items-center px-5 md:px-12 py-20"
    >
      <h1
        class="flex-auto font-display text-white text-center text-4xl md:text-6xl"
      >
        {{ title }}.
        <br />
        {{ subtitle }}.
      </h1>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: false,
      default: '',
    },
    heroUrl: {
      type: String,
      required: false,
      default: '',
    },
  },
}
</script>

<style lang="pcss">
.ch-project__header {
  min-height: 80vh;
  background-size: cover;
  background-position: center;
}
</style>
