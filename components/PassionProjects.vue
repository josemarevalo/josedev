<template>
  <Container>
    <div class="text-left md:ml-1 mt-[50px]">
      <h1 class="font-serif text-[#1d1d1d] text-4xl md:text-5xl">
        Passion Projects
      </h1>

      <div class="passion-projects__cards">
        <ProjectCard
          v-for="project in projects"
          :key="project.idx"
          :title="project.title"
          :categories="project.categories"
          :excerpt="project.excerpt"
          :image="project.image"
          :type="project.type"
        />
      </div>
    </div>
  </Container>
</template>

<script>
import Container from '@/components/Container.vue'
import ProjectCard from '@/components/ProjectCard.vue'

export default {
  name: 'PassionProjects',
  components: {
    Container,
    ProjectCard,
  },
  data() {
    return {
      projects: [
        {
          title: 'Workshops Marketplace',
          categories: ['Django', 'Bootstrap', 'Vue.js'],
          excerpt: 'Creative Workshops Marketplace and Booking System.',
          image: {
            src: 'images/Talleru.png',
            alt: "Woman's hands knitting",
          },
          type: 'Full Stack',
        },
        {
          title: 'Sleep Coaching App',
          categories: ['Django', 'Moment.js', 'Vue.js'],
          excerpt: 'Health Consulting Manager and Sleep Trackking App.',
          image: {
            src: 'images/Sleep-Coaching.png',
            alt: 'Baby sleeping on the side',
          },
          type: 'Full Stack',
        },
        {
          title: 'Inventory Report',
          categories: ['Python', 'Lambda', 'Pandas'],
          excerpt: 'Serverless Asynchronous Reporting From eBay’s Trading API.',
          image: {
            src: 'images/Inventory_Report.png',
            alt: 'Warehouse shelves',
          },
          type: 'Backend',
        },
        {
          title: 'Sports Bets Scraper',
          categories: ['Python', 'Selenium', 'SQLAlchemy'],
          excerpt: 'Multithreading Scraper and Bets Replication Bot.',
          image: {
            src: 'images/Sports_Bet.png',
            alt: "Woman's hands knitting",
          },
          type: 'Backend',
        },
      ],
    }
  },
}
</script>

<style lang="postcss">
.passion-projects__cards {
  @apply lg:mt-[10px] grid grid-cols-1 lg:grid-cols-2 lg:gap-[20px] pb-[60px];
}
</style>
