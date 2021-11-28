<template>
  <div class="row row-cols-3">
    <div class="cardCar col" v-for="course in courses" :key="course.title">
      <img :src="require('../assets/img/' + course.img)" class="w-100" alt="" />
      <h4 class="fs-5 text-center pt-3 titlecard">{{ course.title }}</h4>
      <div class="text-center">
        <button class="rounded-pill ctaLearn">
          {{ course.ctaInfo }}
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    courses: Array,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.titlecard {
  color: $coursesTxt_color;
}
.ctaLearn {
  background-color: #e6eaed;
  border: 3px solid $coursesTxt_color;
  color: $coursesTxt_color;
}
</style>