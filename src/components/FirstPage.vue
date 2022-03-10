<template>
  <v-container class="mt-16 pt-16" fluid style="height: 90vh">
    <v-row style="height: 100%">
      <v-col cols="6" class="d-flex flex-column justify-center">
        <div class="ml-16">
          <p
            class="text-left pl-10"
            style="font-weight: 700; font-size: 3.75rem; line-height: 120%"
          >
            Build a professional resume for free
          </p>
          <p
            class="text-h6 font-weight-medium pl-10"
            style="max-width: 27rem; margin-bottom: 2.25rem"
          >
            Create your resume easily with our free builder and professional
            templates.
          </p>
          <v-btn color="blue" dark large class="ml-10"
            ><span class="text-capitalize text-h6">Create my resume</span>
          </v-btn>
        </div>
      </v-col>
      <v-col cols="6" class="d-flex align-center"
        ><img style="height: 100%" src="../../public/home.webp"
      /></v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "FirstPage",
};
</script>
