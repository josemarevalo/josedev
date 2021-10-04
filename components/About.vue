<template>
  <div class="wrapper">
    <div class="black-bg"></div>

    <div class="rubik hidden md:block md:w-6/12 relative">
      <img
        src="~/assets/images/Rubik_Cube.png"
        class="w-full h-full object-cover absolute"
      />
      <div class="w-full h-full bg-gradient-to-r from-[#1d1d1d] absolute" />
    </div>

    <div class="h-full w-full absolute">
      <Container>
        <div class="about-content">
          <h2 class="font-serif text-4xl md:text-5xl text-center md:text-left">
            About
          </h2>

          <div class="about__content">
            <p>
              José is a Software Engineer who is passionate about
              <span class="underline">solving real life problems</span
              >—efficiently.
            </p>
            <p class="mt-[30px] lg:mt-[40px]">
              He loves creating tidy solutions to help businesses bring their
              <span class="underline">ideas into reality</span>, improve their
              processes, and ultimately scale.
            </p>

            <div
              class="about__link-buttons flex flex-col lg:flex-row mt-[30px]"
            >
              <a href="#" class="about__button-link-item">LinkedIn</a>
              <a href="#" class="about__button-link-item lg:mx-4">GitHub</a>
              <a href="#" class="about__button-link-item">Resume</a>
            </div>
          </div>
        </div>
      </Container>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
}
</script>

<style lang="postcss">
.wrapper {
  /* Super hacky by-eye heights */
  @apply flex flex-row relative h-[620px] md:h-[700px] lg:h-[600px];
}
.black-bg {
  @apply bg-[#1d1d1d] w-full md:w-6/12;
}
.about-content {
  @apply text-[#f9f9f9] mt-[50px] mb-[60px] lg:mt-[80px] lg:mb-[109px] md:w-6/12 md:pr-[24px];
}
.underline {
  text-decoration-color: #28f3c3;
}
.about__button-link-item {
  @apply border-2 py-[6px] lg:py-[8px] px-[24px] lg:px-[20px] rounded-lg mt-[8px] hover:bg-[#f9f9f9] hover:text-[#1d1d1d] text-2xl font-semibold text-center w-full;
}
.about__content {
  @apply text-2xl mt-[30px] lg:mt-[40px] text-center md:text-left;
}
</style>
