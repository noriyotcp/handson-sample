<template>
  <sample :title="indexTitle">
    Hello slot!
    <div slot="named">
      named slot
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
