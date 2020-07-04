<template>
  <v-app dark>
    <v-app-bar fixed app>
      <!-- <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn> -->
      <v-toolbar-title>Self Introduction</v-toolbar-title>
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer app height="32">
      <v-col class="text-center py-0"
        >&copy; {{ new Date().getFullYear() }} papi-tokei all rights
        reserved</v-col
      >
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>
