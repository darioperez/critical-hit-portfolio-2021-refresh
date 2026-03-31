<template>
  <footer class="ch-footer py-20 px-12 bg-black text-gray-700">
    <div
      class="flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-4"
    >
      <img
        src="/DP - Portrait - SM.jpg"
        alt="Portrait"
        class="w-16 h-16 rounded-full object-cover"
      />
      <div class="text-center md:text-left">
        <p>Darío Pérez 😼 {{ currentYear }}</p>
        <p class="mt-2 text-sm">
          <a
            href="mailto:dddarioperezzz@gmail.com"
            class="hover:text-gray-400 transition-colors"
          >
            dddarioperezzz@gmail.com
          </a>
        </p>
      </div>
    </div>
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
