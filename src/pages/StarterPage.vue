<template>
  <div class="background-page">
    <v-sheet color="transparent" class="header" id="header">
      <v-container>
        <v-row justify="center">
          <v-col cols="12">
            <v-img
              src="../../public/images/project/text-the-battle.png"
              alt="The battle for APRs"
              max-width="357"
              class="mx-auto"
            ></v-img>
          </v-col>

          <v-col cols="12" md="9" sm="12">
            <v-img
              src="../../public/images/project/text-select.png"
              alt="Select your fraction, farm your army and battle for the Dragon's gold!"
              max-width="589"
              class="mx-auto"
            ></v-img>
          </v-col>
        </v-row>

        <v-row class="mb-md-9">
          <v-col cols="12">
            <v-img
              src="../../public/images/project/image-background-farm-now.png"
              alt="The battle for APRs"
              max-width="832"
              class="mx-auto"
            ></v-img>
            <v-img
              @click="goToApp"
              src="../../public/images/project/btn-farm-now.png"
              alt="btn-farm-now"
              max-width="248"
              class="mx-auto btn-farm-now cursor-pointer"
            ></v-img>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>

    <v-sheet color="transparent" id="box" class="mt-md-n9 mt-sm-n6">
      <v-container>
        <v-row justify="center">
          <v-col cols="12">
            <v-img
              src="../../public/images/project/image-box.png"
              alt="The most innovative gamified farming protocol on BSC"
              max-width="971"
              class="mx-auto"
            ></v-img>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>

    <v-sheet color="transparent" id="fractions" class="mt-md-n9">
      <v-container>
        <v-row justify="center">
          <v-col cols="12">
            <v-img
              src="../../public/images/project/text-fractions.png"
              alt="fractions"
              max-width="823"
              class="mx-auto"
            ></v-img>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>

    <v-sheet color="transparent" id="collectibles" class="mt-md-9">
      <v-container>
        <v-row justify="center">
          <v-col cols="12">
            <v-img
              src="../../public/images/project/war-collectibles.png"
              alt="fractions"
              max-width="788"
              class="mx-auto"
            ></v-img>
          </v-col>
        </v-row>

        <v-row class="mb-md-9">
          <v-col
            cols="6"
            md="2"
            sm="4"
            v-for="collectible in collectibles"
            v-bind:key="collectible.name"
          >
            <v-img
              :src="`/images/project/collectibles/${collectible.img}`"
              :alt="`collectible-${collectible.name}`"
              max-width="236"
              max-height="385"
              class="mx-auto"
            ></v-img>
            <h3 class="text-center text-collectible">{{ collectible.name }}</h3>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>
  </div>
</template>

<script>
export default {
  data() {
    return {
      urlAPP: process.env.VUE_APP_LINK_APP,
      collectibles: [
        {
          img: "nft-01.png",
          name: "Dragon Slayer",
        },
        {
          img: "nft-02.png",
          name: "Death by Gold",
        },
        {
          img: "nft-03.png",
          name: "The Conqueror",
        },
        {
          img: "nft-04.png",
          name: "War Hero",
        },
        {
          img: "nft-05.png",
          name: "Bloody Battle",
        },
        {
          img: "nft-06.png",
          name: "Memorable Victory",
        },
        {
          img: "nft-07.png",
          name: "Great Reinforcement",
        },
        {
          img: "nft-08.png",
          name: "The legend - Corp",
        },
        {
          img: "nft-09.png",
          name: "The legend - Degen",
        },
      ],
    };
  },

  methods: {
    goToApp() {
      return (window.location = `${this.urlAPP}`);
    },
  },
};
</script>

<style scoped>
.background-page {
  background-image: url("/images/project/background-page.jpg");
  background-size: cover;
}
.header {
  padding: 120px 0px 0px 0px;
  background-image: url("/images/project/fill-farm.png");
  background-size: cover;
}
.btn-farm-now {
  margin-top: -100px;
}
.text-collectible {
  color: #f6ff00;
  background: linear-gradient(180deg, #f6ff00 0%, #ffb800 100%);
  text-shadow: 0px 4px 4px rgb(0 0 0 / 25%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* mobile */
@media screen and (max-width: 959px) {
  .btn-farm-now {
    margin-top: 0px;
    width: 50%;
  }
}
</style>
