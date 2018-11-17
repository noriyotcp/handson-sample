<template>
  <sample :title="indexTitle">
    <div class="come">
      slot example
    </div>
  </sample>
</template>

<script>
import Sample from '~/components/Sample.vue'

export default {
  components: {
    Sample
  },
  data() {
    return {
      indexTitle: 'Nuxt.js data'
    }
  }
}
</script>

<style>
</style>
