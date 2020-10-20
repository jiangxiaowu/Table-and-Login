<template>
  <div class="home">
    <v-img
      dark
      max-height="500px"
      src="https://images.unsplash.com/photo-1505238680356-667803448bb6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div
                :class="{
                  'display-2 font-weight-bold ': $vuetify.breakpoint.smAndUp,
                  'title font-weight-bold': $vuetify.breakpoint.smAndDown,
                }"
              >
                Welcome to my page.
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container class="mt-5">
      <v-layout wrap>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="about">This is me</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{ aboutText }}</div>
          <div class="body-1 mt-3">Anyway I hope you have a great day !</div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="portfolio" right>
            My Work
          </div>
        </v-flex>

        <v-flex xs12 class="mt-5">
          <v-layout wrap>
            <template v-for="(app, i) in apps">
              <v-flex :key="i" xs12 sm6 md4>
                <PPortfolioApp :app="app" />
              </v-flex>
            </template>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="display-1 font-weight-bold" id="contact">
            Send me a message... :)
          </div>
        </v-flex>
        <template v-for="(contact, i) in contactLinks">
          <v-flex sm6 md4 xs12 :key="i">
            <PContactInfo :contact="contact" />
          </v-flex>
        </template>
        
      </v-layout>
      <v-flex class="upbutton">
          <v-btn @click="$vuetify.goTo('#home')">
            <v-icon large color="black darken-2"
              >mdi-arrow-up-bold-box-outline</v-icon
            ></v-btn
          >
        </v-flex>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import PPortfolioApp from "@/components/homepage/PPortfolioApp.vue";
import PContactInfo from "@/components/homepage/PContactInfo.vue";

export default {
  name: "home",
  components: {
    PPortfolioApp,
    PContactInfo,
  },

  data() {
    return {
      aboutText:
        "I'm a new coders, I enjoy building code in my free time when I'm not doing much. Looking to get into machine learning and trying to automate as many things as possible. I'm not very smart, just curious to see how things work. I'm also not that good of a writer as you can see.",
      apps: [
        {
          name: "Music webpage",
          path: "/music",
          price: "Free",

          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "",
            },
          ],
          description:
            "This ie a music playing page, although it only has three songs.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "",
            },
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: "",
          },
        },
        {
          name: "Weather webpage",
          path: "/weather",
          price: "Free",
          logo: "music-logo.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "",
            },
          ],
          description:
            "This is a weather page, currently only supports English and Pinyin search .",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "",
            },
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: "",
          },
        },
        {
          name: "FlyBird",
          path: "/flybird",
          price: "Free",
          logo: "baguette-logo.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "",
            },
          ],
          description: "A popular mobile game, the game is very interesting.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "",
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: "",
            },
            {
              name: "Canvas",
              icon: "mdi-cordova",
              link: "",
            },
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: "https://github.com/jiangxiaowu/flappy-bird",
          },
        },
        {
          name: "Calculator",
          path: "/cal",
          price: "Free",
          logo: "facebook-logo.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https://uzirthapa.github.io/facebook-ui/dist/",
            },
          ],
          description: "It is just a single page calculator.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "",
            },
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: "https://github.com/jiangxiaowu/VueCalculator",
          },
        },
      ],
      contactLinks: [
        {
          name: "Github",
          value: "jiangxiaowu",
          link: "https://github.com/jiangxiaowu/",
          icon: "mdi-github",
        },
        {
          name: "Email",
          value: "jiangxiaowu6868@gmail.com",
          link: "mailto:jiangxiaowu6868@gmail.com",
          icon: "mdi-email",
        },
      ],
    };
  },
  created() {
    this.$emit("showBar");
  },
};
</script>
<style scoped>
.upbutton{
   float:right;
   padding: 20px;
}
</style>
