<template>
  <div>
    <v-footer class="footer">
      <v-container fluid>
        <v-row justify="space-between" class="my-3">
          <v-col cols="12" md="3" align-self="center">
            <img
              src="/images/project/logo-small.png"
              alt=""
              height="70"
              class="mr-1"
            />
            <div class="my-1 white--text">
              © All Rights Reserved 2021
            </div>
          </v-col>
          <v-col cols="12" md="3">
            <h5 class="text-h5 white--text mb-3">
              Menu
            </h5>
            <a class="white--text d-block text-decoration-none my-1" href="https://docs.apwars.farm/">
              Documentation
            </a>
            <a
              class="white--text d-block text-decoration-none my-1"
              href="mailto:contact@apwars.farms"
            >
              Contact
            </a>
          </v-col>
          <v-col cols="12" md="3" align-self="center">
            <div>
              <v-btn
                @click="goToWhitepaper()"
                icon
                color="white lighten-3"
                class="ml-2"
                ><v-icon>mdi-file-document-outline</v-icon>
              </v-btn>
              <v-btn
                @click="goToTelegram()"
                icon
                color="white lighten-3"
                class="ml-2"
                ><v-icon>mdi-telegram</v-icon>
              </v-btn>
              <v-btn
                @click="goToTwitter()"
                icon
                color="white lighten-3"
                class="ml-2"
                ><v-icon>mdi-twitter</v-icon>
              </v-btn>
              <v-btn
                @click="goToGithub()"
                icon
                color="white lighten-3"
                class="ml-2"
              >
                <v-icon>mdi-github</v-icon>
              </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </div>
</template>

<script>
export default {
  methods: {
    goToWhitepaper() {
      window.location = "https://medium.com/apwars";
    },

    goToTelegram() {
      window.location = "https://t.me/apwars";
    },

    goToTwitter() {
      window.location = "https://twitter.com/apwars";
    },

    goToGithub() {
      window.location = "https://github.com/apwars";
    },
  },
};
</script>

<style scoped>
.footer {
  background-color: #000000 !important;
}
</style>
