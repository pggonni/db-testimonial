<template>
  <div class="absolute w-full h-full p-8 xl:p-16 flex flex-col justify-center">
    <timer-bar></timer-bar>
    <div class="max-h-75 lg:max-h-full">
      <img :src="logoURL" alt="Client Logo" class="w-logo h-logo max-w-full object-contain">
    </div>
    <div class="w-16 border-b border-gray-400 my-4"></div>
    <div>"{{ clientQuote }}"</div>
    <div class="text-sm text-gray-700 mt-8">{{ quoteAuthor }}</div>
  </div>
</template>

<script>
import TimerBar from "./TimerBar"

export default {
  props: {
    logoURL: {
      type: String,
      required: true,
    },
    brandColor: {
      type: String,
      required: true,
    },
    clientQuote: {
      type: String,
      required: true,
    },
    quoteAuthor: {
      type: String,
      required: true,
    }
  },
  components: {
    'timer-bar': TimerBar,
  }
}
</script>