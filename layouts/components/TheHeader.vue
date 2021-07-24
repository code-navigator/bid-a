<template lang="pug">
  v-app-bar(
    fixed
    app
  )
    v-app-bar-nav-icon(
      @click.stop="toggleDrawer"
    )
    v-toolbar-title(
      v-text="title"
    )
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  methods: {
    // Pass up event to parent component to handle
    toggleDrawer () {
      this.$emit('click')
    }
  }
}
</script>
