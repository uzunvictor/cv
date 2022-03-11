<template>
  <v-row justify="start" class="full-width d-flex flex-column">
    <v-col
      cols="12"
      style="max-height: 50px; margin-top: 15px; margin-bottom: 15px"
      ><p class="white--text text-h6 font-weight-medium">
        Show that you’re more than just your experience
      </p>
    </v-col>
    <v-col class="d-flex flex-row justify-space-between">
      <v-template v-for="img in images" :key="img">
        <v-hover v-slot="{ hover }">
          <v-card :elevation="hover ? 12 : 4" :class="{ 'on-hover': hover }"
            ><v-img :src="img" height="450px" width="350px"></v-img>
            <v-btn
              v-if="hover"
              color="blue"
              dark
              style="
                margin: auto;
                position: absolute;
                top: 40%;
                left: 0;
                right: 0;
                height: 60px;
              "
              max-width="220px"
              ><p class="ma-2 pa-2 text-capitalize text-h6">
                Use this template
              </p></v-btn
            >
          </v-card>
        </v-hover>
      </v-template>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "Skill",

  data() {
    return {
      images: [
        require("@/assets/skill/1.webp"),
        require("@/assets/skill/2.webp"),
        require("@/assets/skill/3.webp"),
      ],
    };
  },
};
</script>

<style>
</style>