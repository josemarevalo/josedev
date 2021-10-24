<template>
  <div class="wrapper">
    <div class="black-bg"></div>

    <div class="rubik hidden md:block md:w-6/12 relative">
      <nuxt-img
        src="/images/Rubik_Cube.webp"
        alt="Rubik Cube"
        loading="lazy"
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
              <a
                href="https://www.linkedin.com/in/josematiasarevalo/"
                target="_blank"
                class="about__button-link-item"
              >
                <span>LinkedIn</span>
                <svg
                  width="16"
                  height="16"
                  viewBox="0 0 16 16"
                  xmlns="http://www.w3.org/2000/svg"
                  class="about__button-link-item-icon"
                >
                  <path
                    d="M13.001 16H2.00098C0.896407 16 0.000976562 15.1046 0.000976562 14V3C0.000976562 1.89543 0.896407 1 2.00098 1H6.00098V3H2.00098V14H13.001V10H15.001V14C15.001 15.1046 14.1055 16 13.001 16ZM7.70098 9.707L6.29098 8.293L12.584 2H9.00098V0H16.001V7H14.001V3.415L7.70098 9.707Z"
                  />
                </svg>
              </a>

              <a
                href="https://github.com/josematiasarevalo"
                target="_blank"
                class="about__button-link-item lg:mx-4"
              >
                <span>GitHub</span>
                <svg
                  width="16"
                  height="16"
                  viewBox="0 0 16 16"
                  xmlns="http://www.w3.org/2000/svg"
                  class="about__button-link-item-icon"
                >
                  <path
                    d="M13.001 16H2.00098C0.896407 16 0.000976562 15.1046 0.000976562 14V3C0.000976562 1.89543 0.896407 1 2.00098 1H6.00098V3H2.00098V14H13.001V10H15.001V14C15.001 15.1046 14.1055 16 13.001 16ZM7.70098 9.707L6.29098 8.293L12.584 2H9.00098V0H16.001V7H14.001V3.415L7.70098 9.707Z"
                  />
                </svg>
              </a>
              <a
                href="/JOSE_Resume.pdf"
                class="about__button-link-item"
                download
              >
                <span>Resume</span>
                <svg
                  width="14"
                  height="20"
                  viewBox="0 0 14 20"
                  xmlns="http://www.w3.org/2000/svg"
                  class="about__button-link-item-icon"
                >
                  <path
                    d="M14 20H0V18H14V20ZM7 16L1 10L2.41 8.59L6 12.17V0H8V12.17L11.59 8.59L13 10L7 16Z"
                  />
                </svg>
              </a>
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
  @apply flex flex-row items-center justify-center border-2 py-[6px] lg:py-[8px] px-[24px] lg:px-[20px] rounded-lg mt-[8px] hover:bg-[#f9f9f9] hover:text-[#1d1d1d] text-2xl font-semibold text-center w-full;
}
.about__button-link-item-icon {
  @apply ml-[8px];
  fill: currentColor;
}
.about__content {
  @apply text-2xl mt-[30px] lg:mt-[40px] text-center md:text-left;
}
</style>
