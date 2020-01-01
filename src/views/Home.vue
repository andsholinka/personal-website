<template>
  <div class="dr-home">
    <v-container>
      <main-appbar></main-appbar>
      <section id="greetings">
        <h1
          class="font-weight-thin text-uppercase dr-text-greetings"
        >
          Welcome <br> to My <br> Personal Website
          <font-awesome-icon class="amber--text" :icon="['fa', 'smile']"></font-awesome-icon>
        </h1>
        <p class="font-weight-light font-italic">"This website is still under construction"</p>
      </section>
      <section id="socials">
        <v-row
          align-content="center"
          justify="center"
        >
          <v-col
            v-for="(social, index) in socials"
            :key="index"
            cols="auto"
          >
            <v-btn
              text
              icon
              class="secondary--text dr-icon"
              :href="social.href"
              :target="social.target"
            >
              <font-awesome-icon :icon="social.icon"></font-awesome-icon>
            </v-btn>
          </v-col>
        </v-row>
      </section>
      <main-footer></main-footer>
    </v-container>
  </div>
</template>

<script>
import MainAppbar from '@/components/MainAppbar.vue';
import MainFooter from '@/components/MainFooter.vue';

export default {
  name: 'home',
  components: {
    MainAppbar,
    MainFooter,
  },
  data() {
    return {
      socials: [
        {
          href: 'https://instagram.com/dianrahmaji',
          icon: ['fab', 'instagram'],
          target: '_blank',
        },
        {
          href: 'https://github.com/dianrahmaji',
          icon: ['fab', 'github'],
          target: '_blank',
        },
        {
          href: 'https://linkedin.com/in/dianrahmaji',
          icon: ['fab', 'linkedin'],
          target: '_blank',
        },
        {
          href: 'mailto:dianrahmaji@mail.ugm.ac.id',
          icon: ['fas', 'envelope'],
          target: '_top',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.dr-home {
  height: 100%;
  width: 100%;
  .dr-text-greetings {
    font-size: 2.5rem; // 4 nice in 1080, 3 rem too small in 1080
  }
  background-color: #E8E8E8;
  .dr-icon {
    font-size: 1.5rem; // 1.5 nice in phone, 2 nice in laptop
  }
}
</style>
