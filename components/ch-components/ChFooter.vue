<template>
  <footer class="ch-footer py-20 px-12 bg-black text-gray-700">
    <div class="text-center">© {{ currentYear }} Critical Hit Studio.</div>
  </footer>
</template>

<script>
export default {
  computed: {
    currentYear() {
      const currentDate = new Date()
      return currentDate.getFullYear()
    },
  },
}
</script>
