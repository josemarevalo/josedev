<template>
  <div class="container">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'Container',
}
</script>

<style lang="postcss" scoped>
.container {
  @apply mx-auto w-full max-w-[1076px] px-[16px] md:px-[24px];
}
</style>
