<template>
  <div class="bg-[#f9f9f9] py-[50px]">
    <Container>
      <h2 class="font-serif text-[#1d1d1d] text-4xl md:text-5xl">
        Testimonials
      </h2>

      <div class="testimonials__cards">
        <TestimonialCard
          v-for="testimonial in testimonials"
          :key="testimonial.idx"
          :text="testimonial.text"
          :author-name="testimonial.authorName"
          :author-role="testimonial.authorRole"
          :author-avatar="testimonial.authorAvatar"
        />
      </div>
    </Container>
  </div>
</template>

<script>
import Container from '@/components/Container.vue'
import TestimonialCard from '@/components/TestimonialCard.vue'

export default {
  name: 'Testimonials',
  components: {
    Container,
    TestimonialCard,
  },
  data() {
    return {
      testimonials: [
        {
          text: 'He built a complex software system for us to manage our inventory, software we continue to use to this day. José is very competent and will be able to perform any task you put to him flawlessly.',
          authorName: 'Rory Fink',
          authorRole: 'CEO — Luna Events',
          authorAvatar: {
            src: '/images/avatars/Rory.jpeg',
            alt: 'Rory Fink',
          },
        },
        {
          text: "José is up there as one of my favourite people to work with, let alone manage. What made José special? He genuinely cared about what he was doing and was always thinking about ways to improve. Jose's attention to detail is amazing and he is a great mix of commerciality, creativity and technicality.",
          authorName: 'Jacob Moran',
          authorRole: 'Agile Coach — ANZ',
          authorAvatar: {
            src: '/images/avatars/Jacob.jpeg',
            alt: 'Jacob Moran',
          },
        },
        {
          text: 'I am so glad that I got to develop my MVP with José! I’m so happy with the product we ended up with—but above all, I’m very happy with the process. I loved working with José!',
          authorName: 'Margarita Silva',
          authorRole: 'CEO — Zomno App',
          authorAvatar: {
            src: '/images/avatars/Margarita.jpeg',
            alt: 'Margarita Silva',
          },
        },
      ],
    }
  },
}
</script>

<style lang="postcss">
.testimonials__cards {
  @apply grid grid-cols-1 gap-4 mt-[30px] lg:mt-[50px] lg:grid-cols-3 items-start;
}
</style>
