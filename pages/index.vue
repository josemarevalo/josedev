<template>
  <div>
    <Navigation />
    <Header />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Navigation from '@/components/Navigation.vue'

export default {
  name: 'Index',
  components: {
    Header,
    Navigation,
  },
}
</script>
