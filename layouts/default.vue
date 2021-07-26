<template lang="pug">
  v-app(
    light
  )
    TheDrawer(
      :drawer="drawer"
      :items="items"
    )

    TheHeader(
      :title="title"
      @click="toggleDrawer"
    )

    TheContent

    TheFooter
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      title: 'Bid Module'
    }
  },
  methods: {
    // Toggle drawer in and out
    toggleDrawer () {
      this.drawer = !this.drawer
    }
  }
}
</script>
