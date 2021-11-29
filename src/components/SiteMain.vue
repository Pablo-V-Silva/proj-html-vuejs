<template>
  <main>
    <FreeLesson />
    <Courses />
    <Referreal />
    <Instructor />
    <TestimonialCarousel />
    <LatestNews />
  </main>
</template>

<script>
import FreeLesson from "./FreeLesson.vue";
import Courses from "./Courses.vue";
import Referreal from "./Referreal.vue";
import Instructor from "./Instructor.vue";
import TestimonialCarousel from "./TestimonialCarousel.vue";
import LatestNews from "./LatestNews.vue";

export default {
  components: {
    FreeLesson,
    Courses,
    Referreal,
    Instructor,
    TestimonialCarousel,
    LatestNews,
  },
};
</script>

<style>
</style>