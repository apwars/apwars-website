<template>
  <div class="menu">

    <v-app-bar class="elevation-0" height="95">
      <v-container class="py-0 px-0 px-sm-2 fill-height">
        <router-link
          to="/"
          class="d-flex align-center text-decoration-none mr-2"
        >
          <img
            src="/images/project/logo-small.png"
            alt=""
            height="70"
            class="mr-1"
          />
        </router-link>

        <v-spacer></v-spacer>

        <div class="d-none d-md-block">
          <a
            :href="`${item.id}`"
            v-for="(item, index) in menu"
            :key="index"
            text
            class="mx-1 v-btn v-btn--text theme--light v-size--default"
          >
            {{ item.title }}
          </a>
        </div>

        <v-spacer></v-spacer>

        <v-btn
          class="d-none d-md-block btn-gotoapp white--text"
          color="black"
          @click="goToApp()"
          large
        >
          Go to App
        </v-btn>
      </v-container>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
      urlAPP: process.env.VUE_APP_LINK_APP,
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
.menu >>> .theme--light.v-app-bar.v-toolbar.v-sheet {
  background-color: #000 !important;
  position: absolute;
}

.btn-gotoapp {
    background: url('/images/project/btn-gotoapp.png') 50% no-repeat;
    background-size: cover;
    height: 70px !important;
    width: 180px;
    font-size: 22px;
}

.btn-gotoapp >>> span {
  padding-left: 30px;
}
</style>
