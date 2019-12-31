<template>
  <v-app-bar
    app
    color="primary"
    dark
    flat
    hide-on-scroll
  >
    <v-toolbar-title class="text-uppercase secondary--text">
      <span class="font-weight-medium">Dian</span>
      <span class="font-weight-light">Rahmaji</span>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn
      target="_blank"
      text
      class="secondary--text hidden-sm-and-down"
    >
      <span>Project</span>
    </v-btn>
    <v-btn
      target="_blank"
      text
      class="secondary--text hidden-sm-and-down"
    >
      <span>About</span>
    </v-btn>
    <v-btn
      target="_blank"
      text
      class="secondary--text hidden-md-and-up"
    >
     <font-awesome-icon icon="ellipsis-v"></font-awesome-icon>
    </v-btn>
  </v-app-bar>
</template>
