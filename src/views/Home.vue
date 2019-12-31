<template>
  <div class="home">
    <v-container>
      <main-appbar></main-appbar>
      <v-btn
        text
        href="https://instagram.com/dianrahmaji"
        target="_blank"
        class="secondary--text icon"
      >
        <font-awesome-icon :icon="['fab', 'instagram']"></font-awesome-icon>
      </v-btn>
      <v-btn
        text
        href="https://github.com/dianrahmaji"
        target="_blank"
        class="secondary--text icon"
      >
        <font-awesome-icon :icon="['fab', 'github']"></font-awesome-icon>
      </v-btn>
      <v-btn
        text
        href="https://linkedin.com/in/dianrahmaji"
        target="_blank"
        class="secondary--text icon"
      >
        <font-awesome-icon :icon="['fab', 'linkedin']"></font-awesome-icon>
      </v-btn>
      <v-btn
        text
        href="mailto:dianrahmaji@mail.ugm.ac.id"
        target="_top"
        class="secondary--text icon"
      >
        <font-awesome-icon :icon="['fas', 'envelope']"></font-awesome-icon>
      </v-btn>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import MainAppbar from '@/components/MainAppbar.vue';

export default {
  name: 'home',
  components: {
    MainAppbar,
  },
};
</script>

<style lang="scss" scoped>
.home {
  height: 100%;
  width: 100%;
  background-color: #E8E8E8;
  .icon { // Fix this
    font-size: 2rem;
    margin: 1rem;
  }
}
</style>
