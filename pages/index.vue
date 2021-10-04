<template>
  <div>
    <Header />
    <PassionProjects />
    <Testimonials />
    <About />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import PassionProjects from '@/components/PassionProjects.vue'
import Testimonials from '@/components/Testimonials.vue'
import About from '@/components/About.vue'

export default {
  name: 'Index',
  components: {
    Header,
    PassionProjects,
    Testimonials,
    About,
  },
}
</script>
