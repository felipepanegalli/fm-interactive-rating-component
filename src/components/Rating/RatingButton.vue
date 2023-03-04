<template>
  <button class="w-12 h-12 rounded-full" :class="(selected === label) ? 'active' : 'link link-hover'">
    <span class="text-md">{{ label }}</span>
  </button>
</template>

<script>
export default {
  name: 'RateButton',
  props: ['label', 'selected']
}
</script>

<style lang="postcss">
.active {
  @apply bg-primary-orange text-neutral-white
}

.link {
  @apply bg-neutral-dark-blue text-neutral-light-grey;
}

.link:hover {
  @apply bg-neutral-medium-grey text-neutral-white
}
</style>
