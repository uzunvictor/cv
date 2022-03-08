<template>
  <div style="background: #eceff1">
    <v-app-bar :elevation="0" color="white" min-height="100px">
      <v-img
        class="ml-2"
        src="../../public/R.png"
        max-width="100px"
        contain
      ></v-img>
      <v-toolbar-title
        class="ma-0 pa-0 blue--text text-h4 mb-1 font-weight-bold"
      >
        myResume</v-toolbar-title
      ><v-spacer></v-spacer>

      <div>
        <v-btn text elevation="0"
          ><span class="text-capitalize text-subtitle-1">Resume</span
          ><v-icon>mdi-chevron-down</v-icon></v-btn
        >
        <v-btn text elevation="0"
          ><span class="text-capitalize text-subtitle-1">Cover Letter</span
          ><v-icon>mdi-chevron-down</v-icon></v-btn
        >
        <v-btn text elevation="0"
          ><span class="text-capitalize text-subtitle-1">Resume Writing</span
          ><v-icon>mdi-chevron-down</v-icon></v-btn
        >
        <v-btn text elevation="0"
          ><span class="text-capitalize text-subtitle-1">Blog</span></v-btn
        >
        <v-btn text elevation="0"
          ><span class="text-capitalize text-subtitle-1">FAQ</span></v-btn
        >
      </div>

      <v-btn text elevation="0">|</v-btn>
      <div>
        <v-btn
          min-height="55px"
          :style="`background: transparent;`"
          elevation="0"
          ><span
            class="
              font-weight-bold
              blue--text
              text--darken-1 text-capitalize text-subtitle-1
              ma-2
            "
            >Log in</span
          ></v-btn
        >
        <v-btn min-height="55px" large class="ma-2" color="blue darken-1" dark
          ><span class="text-capitalize text-subtitle-1 font-weight-bold"
            >Sign Up</span
          ></v-btn
        >
      </div>
    </v-app-bar>
    <first-page />
    <second-page />
  </div>
</template>

<script>
import FirstPage from "../components/FirstPage.vue";
import SecondPage from "../components/SecondPage.vue";

export default {
  name: "Home",

  components: {
    FirstPage,
    SecondPage,
  },
};
</script>

<style scoped>
>>> .v-toolbar__content {
  min-height: 100px;
}

.background {
  background-color: #fff;
}
</style>