<template>
  <v-app dark>
    <TheDrawer
      :drawer="drawer"
      :items="items"
    />

    <TheHeader
      @click="toggleDrawer"
      :title="title"
    />
    <v-app-bar
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title  />
    </v-app-bar>
    <TheContent />
    <TheFooter />
  </v-app>
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
      title: 'Vuetify.js'
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
