<template>
  <section
    id="get-in-touch"
    class="hide-overflow app-background"
  >
    <v-layout>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/contact.png')"
          height="100%"
        />
      </v-flex>
      <v-flex
        xs12
        md6
        pa-5
      >
        <base-bubble-1 />
        <base-heading class="mb-5">
          Get In Touch
        </base-heading>

        <v-sheet
          max-width="600"
          color="transparent"
        >
          <v-text-field
            label="Name"
            box
          />
          <v-text-field
            label="E-mail"
            box
          />
          <v-text-field
            label="Betreff"
            box
          />
          <v-textarea
            label="Ihr Anliegen"
            box
            no-resize
            counter="200"
          />
          <v-checkbox
            v-model="dsgvoAccepted"
            color="primary"
            label="Ich habe die Datenschutzbedingungen gelesen und erkläre mich damit einverstanden."
          />
          <base-btn class="mt-3">
            Absenden
            <v-icon right>
              mdi-send
            </v-icon>
          </base-btn>
        </v-sheet>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    dsgvoAccepted: false
  })
}
</script>
