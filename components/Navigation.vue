<template>
  <nav class="py-[16px] lg:py-[50px] bg-[#1d1d1d]">
    <Container class="flex items-center">
      <span class="text-2xl lg:text-4xl font-serif">
        <span class="text-[#28F3c3]">&#60;</span>JoséDev
        <span class="text-[#28F3c3]">/&#62;</span>
      </span>

      <div class="w-5/12 ml-auto">
        <ul class="flex text-2xl justify-end">
          <li class="mr-10">Projects</li>
          <li class="mr-10">About</li>
          <li>Contact</li>
        </ul>
      </div>
    </Container>
  </nav>
</template>

<script>
import Container from './Container.vue'

export default {
  name: 'Navigation',
  components: { Container },
}
</script>

<style></style>

Container
