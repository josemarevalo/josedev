<template>
  <div class="card">
    <div class="w-full md:w-2/6 lg:w-full">
      <img
        :src="require(`~/assets/${image.src}`)"
        :alt="image.alt"
        class="h-full object-cover"
      />
    </div>

    <div class="card__content flex flex-col">
      <div>
        <p class="text-[#28f3c3]">
          <span v-for="category in categories" :key="category.idx">
            #{{ category }}
          </span>
        </p>

        <h2 class="text-2xl lg:text-3xl mt-[8px] font-bold">
          {{ title }} | {{ type }}
        </h2>

        <p class="text-xl lg:text-2xl mt-[8px]">{{ excerpt }}</p>
      </div>

      <div class="mt-auto flex items-end">
        <button class="card__call-to-action">
          <p class="text-lg lg:text-xl">Learn more</p>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    categories: {
      type: Array,
      required: true,
    },
    excerpt: {
      type: String,
      required: true,
    },
    image: {
      type: Object,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="postcss">
.card {
  @apply mt-[30px] lg:mt-[40px] text-left rounded-xl overflow-hidden shadow-lg flex flex-col md:flex-row lg:flex-col;
}
.card__content {
  @apply bg-[#1d1d1d] text-[#f9f9f9] p-[16px] w-full h-full;
}
.card__call-to-action {
  @apply bg-gray-100 text-[#1d1d1d] py-[6px] lg:py-[10px] px-[24px] lg:px-[40px] rounded mt-[27px] hover:bg-[#28f3c3];
}
</style>
