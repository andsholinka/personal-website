<template>
  <div class="dr-home">
    <v-container style="height: 100%">
      <main-appbar></main-appbar>
      <section id="greetings">
        <v-row
          style="height: 40vh"
          justify="start"
          align-content="end"
        >
          <v-col xs="12" md="6" class="pb-0">
            <h1
              id="greetings-heading"
              class="font-weight-thin text-uppercase dr-text-greetings"
            >
            </h1>
            <!-- <font-awesome-icon class="amber--text" :icon="['fa', 'smile']">
            </font-awesome-icon> -->
            <p class="font-weight-light font-italic">"This website is still under construction"
            </p>
          </v-col>
        </v-row>
      </section>
      <section id="socials">
        <v-row
          align-content="start"
          justify="start"
          style="height: 25vh"
        >
          <v-col
            v-for="(social, index) in socials"
            :key="index"
            cols="auto"
            class="pt-0"
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
import TypeIt from 'typeit';

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
  mounted() {
    this.doTypewriting();
  },
  methods: {
    doTypewriting() {
      const greetings = new TypeIt('#greetings-heading', {
        speed: 50,
        startDelay: 900,
      });

      greetings
        .type('Welcome to')
        .pause(300)
        .type('<br>')
        .pause(300)
        .type('My Personal Website')
        .pause(750)
        .type(' 😊')
        .go();
    },
  },
};
</script>

<style lang="scss" scoped>
.dr-home {
  height: 100%;
  width: 100%;
  .dr-text-greetings {
    font-size: 1.8rem;
    @media only screen and (min-width: 600px) {
      font-size: 2.3rem;
    }
    @media only screen and (min-width: 1264px) {
      font-size: 3.1rem
    }
  }
  background-color: #E8E8E8;
  .dr-icon {
    font-size: 1.5rem;
  }
}
</style>
