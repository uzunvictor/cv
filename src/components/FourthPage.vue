<template>
  <v-row class="d-flex flex-column align-center" style="min-height: 603px">
    <v-col cols="12" class="d-flex flex-column align-center"
      ><p
        class="text-h3 font-weight-medium mt-10 text-center mb-0"
        style="max-width: 850px"
      >
        Get inspired by resume samples from professional resume experts
      </p>
      <p
        class="text-h6 font-weight-medium my-16 text-center mt-3 mb-4"
        style="max-width: 550px"
      >
        Search by job title to find resumes from resume experts that can inspire
        your own resume creation.
      </p>
    </v-col>
    <v-col class="text-center" style="max-width: 1260px">
      <v-btn
        outlined
        class="button-border rounded-xl pa-6 ma-1"
        v-for="button in resumeButtons"
        :key="button"
        ><span class="text-capitalize" style="font-size: 1.125rem">{{
          button
        }}</span></v-btn
      >
    </v-col>
    <v-col class="d-flex justify-center mt-10 mb-16 py-0">
      <v-btn color="blue" dark large><span class="text-capitalize text-subtitle-1 mx-4 my-3" style="font-weight: 700">Explore all Samples</span> </v-btn>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "FourthPage",

  data() {
    return {
      resumeButtons: [
        "Accountant",
        "Security Guard",
        "Mechanical Engineer",
        "JAVA Developer",
        "Designer",
        "Recruiter",
        "Product Manager",
        "Dentist",
        "Digital Marketing",
        "Sales Associate",
        "Management",
        "Phisician Assistant",
        "Front End Developer",
        "Nursing",
        "Civil Engineer",
        "Office Assistant",
        "Photographer",
        "Finance",
        "Teacher",
      ],
    };
  },
};
</script>

<style>
.button-border {
  border: 2px solid rgba(10, 10, 10, 0.253);
}

.v-btn:hover {
  border: 2px solid rgb(17, 89, 223);
}
</style>