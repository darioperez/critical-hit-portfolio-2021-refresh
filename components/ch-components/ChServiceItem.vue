<template>
  <section class="ch-sercive-item flex justify-start items-center text-xl">
    <div
      class="flex-initial flex-shrink-0 w-24 h-24 bg-brand mr-6 flex justify-center items-center"
    >
      <img :src="require(`~/assets/icons/services/${src}.svg`)" alt="" />
    </div>

    <p class="flex-auto">
      {{ label }}
    </p>
  </section>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
  },
}
</script>
