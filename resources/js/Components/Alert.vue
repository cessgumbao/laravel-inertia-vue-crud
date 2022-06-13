<script >
export default {
  props: {
    color: String,
    message: String,
  },
  data() {
    return {
      opacity: "opacity: 0.8"
    }
  },
  mounted() {
    setTimeout(() => {
      this.opacity = "opacity: 0";
    }, 3000);
  }
}
</script>
<template>
  <div class="absolute top-0 right-0 mt-10 mr-10 opacity-80 w-1/3 transition-opacity duration-500 ease-out" :style="opacity">
    <div id="flash-message" class="flex p-4 mb-4 rounded-lg" :class="`bg-${color}-100 dark:bg-${color}-200`" role="alert">
      <svg class="flex-shrink-0 w-5 h-5" :class="`text-${color}-700 dark:text-${color}-800`" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z" clip-rule="evenodd"></path></svg>
      <div class="ml-3 text-sm font-medium" :class="`text-${color}-700 dark:text-${color}-800`">
        {{ message }}
      </div>
    </div>
  </div>
</template>