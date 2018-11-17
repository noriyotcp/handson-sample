<template lang="html">
  <div class="sample">
    <h1>{{ title }}</h1>
    Hello, I'm {{ name }}!
    <div>
      {{ reverseName }}!
    </div>
    <button
      type="button"
      name="button"
      @click="plus">click times: {{ num }}</button>
    <div class="slot">
      <slot />
    </div>
    <div :class="['hide', { seven: num === 7 }]">
      click 7 times
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default Title'
    }
  },
  data() {
    return {
      name: 'noriyotcp',
      num: 0
    }
  },
  computed: {
    reverseName() {
      return this.name
        .split('')
        .reverse()
        .join('')
    }
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;
  &.seven {
    display: block;
  }
}
.slot {
  color: red;
}
</style>
