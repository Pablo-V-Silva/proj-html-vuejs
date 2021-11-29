<template>
  <main>
    <FreeLesson />
    <Courses />
    <Referreal />
    <Instructor />
    <TestimonialCarousel />
    <LatestNews />
    <Email />
  </main>
</template>

<script>
import FreeLesson from "./FreeLesson.vue";
import Courses from "./Courses.vue";
import Referreal from "./Referreal.vue";
import Instructor from "./Instructor.vue";
import TestimonialCarousel from "./TestimonialCarousel.vue";
import LatestNews from "./LatestNews.vue";
import Email from "./Email.vue";

export default {
  components: {
    FreeLesson,
    Courses,
    Referreal,
    Instructor,
    TestimonialCarousel,
    LatestNews,
    Email,
  },
};
</script>

<style>
</style>