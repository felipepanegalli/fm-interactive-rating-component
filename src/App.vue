<template>
  <div class="bg-neutral-very-dark-blue h-full w-full flex items-center justify-center p-6 md:p-0">
    <rating-votes v-if="selected === 0" @selected="(val) => selected = val" />
    <rating-result v-else :rate="selected" />
  </div>
</template>

<script>
import { ref } from 'vue'
import RatingVotes from './components/Rating/RatingVotes.vue'
import RatingResult from './components/Rating/RatingResult.vue'

export default {
  name: 'App',
  components: { RatingVotes, RatingResult },
  setup () {
    const selected = ref(0)
    return { selected }
  }
}
</script>
