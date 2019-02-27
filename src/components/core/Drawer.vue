<template>
  <v-navigation-drawer
    v-model="drawer"
    app
    right
    temporary
  >
    <v-list>
      <v-list-tile
        @click=""
        v-for="(item, i) in navigationItems"
        :key="i"
      >
        <v-list-tile-avatar>
          <v-icon v-text="item.icon"></v-icon>
        </v-list-tile-avatar>

        <v-list-tile-content>
          <v-list-tile-title v-text="item.title"></v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
  import navigationItems from './NavigationItems'

  export default {
    data: () => ({
      navigationItems
    }),
    computed: {
      drawer: {
        get () {
          return this.$store.state.drawer
        },
        set (val) {
          this.$store.commit('setDrawer', val)
        }
      }
    }
  }
</script>

<style
  lang="sass"
  scoped
>

</style>
