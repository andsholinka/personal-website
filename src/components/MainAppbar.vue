<template>
  <v-app-bar
    app
    color="primary"
    dark
    flat
  >
    <v-toolbar-title class="text-uppercase secondary--text">
      <span class="font-weight-medium">Dian</span>
      <span class="font-weight-light">Rahmaji</span>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn
      v-for="(menu, index) in menus"
      :key="index"
      text
      class="secondary--text hidden-sm-and-down"
      router :to="menu.route"
    >
      <span>{{ menu.title }}</span>
    </v-btn>
    <v-menu offset-y>
      <template v-slot:activator="{ on }">
        <v-btn
          target="_blank"
          text
          icon
          v-on="on"
          class="secondary--text hidden-md-and-up"
        >
          <font-awesome-icon icon="ellipsis-v"></font-awesome-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(menu, index) in menus"
          :key="index"
          router :to="menu.route"
        >
          <v-list-item-title>{{ menu.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      menus: [
        { title: 'Projects', route: '#' },
        { title: 'Blog', route: '#' },
        { title: 'About', route: '#' },
      ],
    };
  },
};
</script>
