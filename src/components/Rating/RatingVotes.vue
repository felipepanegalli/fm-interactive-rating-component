<template>
  <div
    class="w-414 p-8 rounded-3xl bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] bg-neutral-radial-1 bg-neutral-radial-2">
    <p class="w-12 h-12 bg-neutral-dark-blue rounded-full text-neutral-light-grey flex items-center justify-center mb-6">
      <img src="../../..//src/assets/images/icon-star.svg" alt="Star">
    </p>
    <h1 class=" text-neutral-white text-xl mb-2">How did we do?</h1>
    <p class=" text-neutral-medium-grey text-sm">
      Please let us know how we did with your support<br class="hidden md:block">
      request. All feedback is appreciated to help us<br class="hidden md:block">
      improve our offering!</p>
    <div class="w-full flex justify-between my-6">
      <rate :label="1" :selected="selected" @click="() => { selected = 1 }" />
      <rate :label="2" :selected="selected" @click="() => { selected = 2 }" />
      <rate :label="3" :selected="selected" @click="() => { selected = 3 }" />
      <rate :label="4" :selected="selected" @click="() => { selected = 4 }" />
      <rate :label="5" :selected="selected" @click="() => { selected = 5 }" />
    </div>
    <button @click="$emit('selected', selected)" :disabled="selected === 0"
      class=" bg-primary-orange text-neutral-white p-3 rounded-full w-full text-sm"
      :class="selected === 0 ? 'opacity-25 cursor-not-allowed' : 'hover:bg-neutral-white hover:text-primary-orange'">
      <span class="text-md">SUBMIT</span></button>
  </div>
</template>

<script>
import { ref } from 'vue'
import Rate from './RatingButton.vue'

export default {
  name: 'RateContainer',
  components: { Rate },
  setup () {
    const selected = ref(0)
    return { selected }
  }
}
</script>
