<template>
  <div
    class="w-414 p-8 rounded-3xl bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] bg-neutral-radial-1 bg-neutral-radial-2">
    <div class="w-full text-center flex flex-col gap-4">
      <img src="../../assets/images/illustration-thank-you.svg" alt="Thank You" class=" w-1/2 flex self-center py-2" />
      <span class="bg-neutral-dark-blue rounded-full text-primary-orange py-2 px-4 my-2">
        You selected {{ rate ?? 0 }} out of 5
      </span>
      <h1 class="text-neutral-white text-xl">Thank you!</h1>
      <p class=" text-neutral-medium-grey text-sm pb-3">
        We appreciate you taking the time to give a rating.<br class="hidden md:block">
        If you ever need more support, don't hesitate to<br class="hidden md:block">
        get in touch!</p>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'RateContainer',
  props: ['rate'],
  setup () {
    const selected = ref(0)
    return { selected }
  }

}
</script>
