 <template>
  <v-container fluid style="height: 120vh" class="mx-16">
    <v-row class="ma-16 mb-3 d-flex justify-center">
      <p
        class="text-h3 font-weight-bold text-center my-5 mx-16"
        style="max-width: 700px"
      >
        Land your dream job with the help of our resume builder
      </p></v-row
    >
    <v-row>
      <v-col cols="7">
        <v-img min-width="770px" src="../../public/second.webp"> </v-img>
      </v-col>
      <v-col cols="5" class="d-flex flex-column justify-start pt-10">
        <v-btn
          elevation="0"
          v-for="item in items"
          :key="item.icon"
          min-height="100px"
          text
          class="d-flex justify-start"
          ><v-icon class="ma-5" :color="item.color" large left>{{
            item.icon
          }}</v-icon
          ><span class="custom-transform-class text-none text-h4">{{
            item.title
          }}</span></v-btn
        >
      </v-col>
    </v-row>
  </v-container>
</template>
 
 <script>
export default {
  name: "SecondPage",

  data() {
    return {
      items: [
        {
          icon: "mdi-download-outline",
          color: "red",
          title: "Free Download",
        },
        {
          icon: "mdi-check-decagram-outline",
          color: "cyan",
          title: "Excellent design",
        },
        {
          icon: "mdi-draw-pen",
          color: "purple",
          title: "Easy to compose",
        },

        {
          icon: "mdi-view-grid-outline",
          color: "green",
          title: "Intuitive Resume Builder",
        },
        {
          icon: "mdi-briefcase-outline",
          color: "blue",
          title: "A Resume Tailored to your job",
        },
      ],
    };
  },
};
</script>
 
 <style>
</style>