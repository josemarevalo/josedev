<template>
  <div class="bg-[#1d1d1d] text-gray-100 absolute w-full">
    <Navigation />

    <div>
      <Container>
        <div class="header__wrapper">
          <div
            class="header__content w-full lg:w-8/12 text-center lg:text-left"
          >
            <h1 class="text-5xl lg:text-8xl font-serif mt-[28px] lg:mt-none">
              José M. Arévalo
            </h1>

            <h2 class="text-2xl lg:text-3xl mt-[30px] lg:mt-[40px]">
              Full Stack Software Developer
            </h2>

            <button class="header__call-to-action">
              <p class="text-xl">Let's have a chat</p>
            </button>
          </div>

          <div class="w-full lg:w-4/12">
            <div class="header__picture">
              <img
                src="~/static/images/avatars/Jose.png"
                alt="jose-profile-picture"
                class="w-full h-full aspect-w-1 aspect-h-1"
              />
            </div>
          </div>
        </div>
      </Container>
    </div>
  </div>
</template>

<script>
import Container from './Container.vue'
import Navigation from './Navigation.vue'

export default {
  name: 'Header',
  components: {
    Container,
    Navigation,
  },
}
</script>

<style lang="postcss">
.header__wrapper {
  @apply flex flex-col-reverse lg:flex-row mt-[70px] lg:mt-[120px] pb-[154px];
}
.header__picture {
  @apply border-gray-100 border-8 rounded-full overflow-hidden w-6/12 lg:w-auto mx-auto lg:mx-[0px];
}
.header__call-to-action {
  @apply bg-gray-100 text-[#1d1d1d] py-2 px-10 rounded mt-[40px];
}
</style>
