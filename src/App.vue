<template>
  <v-app
    dark
    class="app-background"
  >
    <core-drawer />

    <core-toolbar />

    <core-view />

    <core-footer />
  </v-app>
</template>

<script>
export default {
  components: {
    CoreDrawer: () => import('@/components/core/Drawer'),
    CoreFooter: () => import('@/components/core/Footer'),
    CoreToolbar: () => import('@/components/core/Toolbar'),
    CoreView: () => import('@/components/core/View')
  }
}
</script>

<style lang="sass">
  .app-background
    background-color: #1B1D1F
</style>
