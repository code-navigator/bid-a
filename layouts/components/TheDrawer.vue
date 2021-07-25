<template lang="pug">
  v-navigation-drawer(
    v-model="position"
    fixed
    app
  )
    v-list
      v-list-item(
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        router
        exact
      )
        v-list-item-action
          v-icon {{ item.icon }}
        v-list-item-content
          v-list-item-title(
            v-text="item.title"
          )
</template>

<script>
export default {
  props: {
    drawer: {
      type: Boolean
    },
    items: {
      type: Array,
      required: true
    }
  },
  computed: {
    position: {
      get() {
        return this.drawer
      },
      set() {

      }
    }
  }
}
</script>
