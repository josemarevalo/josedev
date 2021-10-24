<template>
  <div class="testimonial-card md:flex md:flex-row lg:flex-col">
    <div class="-mt-16 md:mt-[24px] lg:-mt-16">
      <div class="testimonial-card__avatar-border">
        <nuxt-img
          :src="authorAvatar.src"
          :alt="authorAvatar.alt"
          sizes="sm:136px"
          loading="lazy"
          class="w-[120px] aspect-w-1 aspect-h-1 rounded-full"
        />
      </div>
    </div>

    <div class="testimonial-card__content mt-[24px] md:ml-[24px] lg:ml-0">
      <p class="">"{{ text }}"</p>
      <div class="mt-[30px] lg:mt-[40px] font-bold">
        <p>{{ authorName }}</p>
        <p>{{ authorRole }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TestimonialCard',
  props: {
    text: {
      type: String,
      required: true,
    },
    authorName: {
      type: String,
      required: true,
    },
    authorRole: {
      type: String,
      required: true,
    },
    authorAvatar: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="postcss">
.testimonial-card {
  @apply bg-white pb-[24px] px-[24px] md:pl-[16px] lg:pl-[24px] rounded-xl shadow text-xl text-[#1d1d1d] mt-20 md:mt-0 lg:mt-20;
}
.testimonial-card__avatar-border {
  @apply flex items-center justify-center rounded-full overflow-hidden w-[136px] h-[136px] mx-auto bg-gradient-to-br from-[#28f3c3] to-[#9a65d9] shadow-md;
}
</style>
