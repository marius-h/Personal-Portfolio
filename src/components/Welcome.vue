<template>
  <section
    id="welcome"
    class="hide-overflow mainbody"
  >
    <v-layout fill-height>
      <v-flex
        xs12
        md6
        align-content-space-between
        layout
        :pa-5="$vuetify.breakpoint.smAndDown"
        wrap
      >
        <v-layout
          fill-height
          align-center
          justify-center
        >
          <v-flex
            xs10
            md7
          >
            <base-heading>Marius Höfler</base-heading>
            <base-subheading>Frontend-Entwickler</base-subheading>
            <base-btn class="mt-4">
              Kontaktieren
            </base-btn>
          </v-flex>
        </v-layout>

        <base-bubble-2
          style="transform: rotate(180deg) translate(-200px, -15%)"
        ></base-bubble-2>
      </v-flex>

      <v-flex
        hidden-sm-and-down
        md6
      >
        <base-bubble-1 class="blob-br"></base-bubble-1>
      </v-flex>
    </v-layout>
  </section>
</template>

<style
  lang="sass"
  scoped
>
  .mainbody
    height: 100vh

    .blob-br
      position: absolute
      left: 14.67%
      right: 19.82%
      top: 16.11%
      bottom: 20.69%
</style>
