<template>
  <nav class="bg-[#1d1d1d] text-[#f9f9f9]">
    <Container class="relative lg:flex lg:justify-between lg:items-center">
      <div class="flex items-center justify-between pt-[16px] lg:py-[50px]">
        <span class="text-2xl lg:text-4xl font-serif">
          <span class="text-[#28F3c3]">&#60;</span>JoséDev
          <span class="text-[#28F3c3]">/&#62;</span>
        </span>

        <button
          type="button"
          class="text-gray-[#f9f9f9] hover:text-white outline-none lg:hidden"
          @click="isOpen = !isOpen"
        >
          <svg
            viewBox="0 0 24 16"
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8 fill-current"
          >
            <path
              v-if="!isOpen"
              d="M24 16H12V13.3333H24V16ZM24 9.33333H0V6.66667H24V9.33333ZM24 2.66667H0V0H24V2.66667Z"
            />
            <path
              v-else
              d="M12.59 0L7 5.59L1.41 0L0 1.41L5.59 7L0 12.59L1.41 14L7 8.41L12.59 14L14 12.59L8.41 7L14 1.41L12.59 0Z"
            />
          </svg>
        </button>
      </div>

      <div class="nav__links" :class="isOpen ? 'block' : 'hidden'">
        <a href="#" class="nav__link-item lg:mr-10">Projects</a>
        <a href="#" class="nav__link-item lg:mr-10">About</a>
        <a href="#" class="nav__link-item">Contact</a>
      </div>
    </Container>
  </nav>
</template>

<script>
import Container from '@/components/Container.vue'

export default {
  name: 'Navigation',
  components: { Container },
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>

<style lang="postcss">
.nav__links {
  @apply absolute text-lg lg:text-2xl lg:justify-end pt-2 pb-4 lg:p-0 -ml-2 lg:ml-0 bg-[#1d1d1d] w-[calc(100%-16px)] lg:block lg:w-auto lg:static z-40;
}
.nav__link-item {
  @apply block py-1 px-2 hover:bg-gray-600 rounded mt-1 lg:inline;
}
</style>
