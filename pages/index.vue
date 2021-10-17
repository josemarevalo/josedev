<template>
  <div>
    <Header />
    <PassionProjects />
    <Testimonials />
    <About />
    <Contact />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import PassionProjects from '@/components/PassionProjects.vue'
import Testimonials from '@/components/Testimonials.vue'
import About from '@/components/About.vue'
import Contact from '@/components/Contact.vue'

export default {
  name: 'Index',
  components: {
    Header,
    PassionProjects,
    Testimonials,
    About,
    Contact,
  },
}
</script>
