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
    <component :is="isActive" />
  </v-container>
</template>

<script>
import Education from "./Education.vue";
import Skill from "./Skill.vue";
import Experience from "./Experience.vue";
import Personality from "./Personality.vue";

export default {
  components: { Education, Skill, Experience, Personality },
  name: "ThirdPage",

  data() {
    return {
      items: ["Education", "Skill", "Experience", "Personality"],
      isActive: "Education",
      templateTitle: "title",
    };
  },
};
</script>

<style scoped>
.third-background {
  background-image: url("../../../public/back.png");
  min-height: 100vh;
  background-size: 140%;
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