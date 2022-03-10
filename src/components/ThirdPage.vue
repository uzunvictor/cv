<template>
  <v-container fluid class="third-background d-flex flex-column align-center">
    <p class="white--text text-h3 font-weight-medium my-16">
      Every detail on your resume, built to perfection
    </p>
    <v-row
      style="
        width: 100%;
        max-width: 1400px;
        max-height: 55px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.438);
      "
      justify="space-between"
      class="px-16 mt-10"
      align="end"
    >
      <template v-for="item in items">
        <v-col :key="item" class="d-flex justify-center align-end pb-0">
          <v-btn
            text
            :class="{ active: isActive === item }"
            @click="isActive = item"
          >
            <p class="white--text text-h5 text-uppercase font-weight-medium">
              {{ item }}
            </p>
          </v-btn>
        </v-col>
      </template>
    </v-row>
    <v-row justify="start" class="full-width d-flex flex-column">
      <v-col
        cols="12"
        style="max-height: 50px; margin-top: 15px; margin-bottom: 15px"
        ><p class="white--text text-h6 font-weight-medium">
          Highlight the academic background that makes you shine
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
  </v-container>
</template>

<script>
export default {
  name: "ThirdPage",

  data() {
    return {
      items: ["Education", "Skill", "Experience", "Personality"],
      images: [
        require("@/assets/1.webp"),
        require("@/assets/2.webp"),
        require("@/assets/3.webp"),
      ],
      isActive: "Education",
      templateTitle: "title",
    };
  },
};
</script>

<style scoped>
.third-background {
  background-image: url("../../public/back.png");
  min-height: 100vh;
  background-size: 100%;
}

.active {
  border-bottom: 2px solid white;
  background: transparent;
}

.v-btn::before {
  background-color: transparent;
}

.full-width {
  min-width: 76%;
}

.v-card {
  transition: all 0.2s ease-in-out;
}

.v-card:hover {
  transform: scale(1.02);
}
</style>