<template>
  <v-container class="pa-0"
    ><v-row class="d-flex flex-column mb-16"
      ><v-col class="d-flex justify-center">
        <span class="text-h3 font-weight-medium" style="margin: 80px 0"
          >Why build my resume with Resume.com?</span
        >
      </v-col>
      <v-col class="d-flex flex-row justify-center"
        ><template v-for="item in items"
          ><v-card
            :key="item.title"
            min-height="228px"
            width="434px"
            :elevation="0"
            class="px-4"
          >
            <v-img :src="item.img" max-height="45px" max-width="45px"></v-img>
            <v-card-title class="text-h5 font-weight-bold pl-0">{{
              item.title
            }}</v-card-title>
            <v-card-text class="pl-0" style="font-size: 1.125rem">{{
              item.text
            }}</v-card-text>
          </v-card></template
        ></v-col
      >
    </v-row></v-container
  >
</template>

<script>
export default {
  name: "FifthPage",

  data() {
    return {
      items: [
        {
          img: require("@/assets/fifth_page/1.webp"),
          text: "No gimmicks, no freemium features, no joke. Get everything you need to build a professional resume that shows off your best qualities to help you land your next job.",
          title: "We’re actually free",
        },
        {
          img: require("@/assets/fifth_page/2.webp"),
          text: "Rest assured that the templates you find on Resume.com are the best around. Based on data from what employers want to see in candidates, we’ve created our templates with hiring in mind.",
          title: "Data-Driven Templates",
        },
        {
          img: require("@/assets/fifth_page/3.webp"),
          text: "With your resume ready for top employers, easily share with millions of interested employers on Indeed, the world’s #1 job site.",
          title: "Get Seen",
        },
      ],
    };
  },
};
</script>

<style>
</style>