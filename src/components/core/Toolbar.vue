<template>
  <v-toolbar
    v-scroll="onScroll"
    :color="isTransparent ? 'transparent' : '#1B1D1F'"
    app
    flat
  >
    <v-toolbar-title>
      <img
        src="@/assets/logo.svg"
        alt=""
        height="30"
      >
    </v-toolbar-title>
    <v-spacer />

    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn
        v-for="(item, i) in navigation"
        :key="i"
        text
      >
        {{ item.title }}
      </v-btn>
      <v-btn
        height="40"
        color="primary"
        class="ml-2"
      >
        <v-icon left>
          mdi-email
        </v-icon>
        Kontakt
      </v-btn>
    </v-toolbar-items>
    <v-toolbar-side-icon
      @click.stop="toggleDrawer"
      class="hidden-md-and-up"
    />
  </v-toolbar>
</template>

<script>
  import navigationItems from './NavigationItems'

  export default {
    data: () => ({
      isTransparent: true,
      drawer: false,
      navigation: navigationItems.slice(0, navigationItems.length - 1)
    }),

    methods: {
      toggleDrawer () {
        this.$store.commit('toggleDrawer')
      },
      onScroll () {
        this.isTransparent = window.pageYOffset < 200
      }
    }
  }
</script>
