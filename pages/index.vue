<template>
  <div>
    <Header />
    <PassionProjects />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import PassionProjects from '@/components/PassionProjects.vue'

export default {
  name: 'Index',
  components: {
    Header,
    PassionProjects,
  },
}
</script>
