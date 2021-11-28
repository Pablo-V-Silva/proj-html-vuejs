<template>
  <main>
    <FreeLesson />
    <Courses />
    <Referreal />
    <Instructor />
    <TestimonialCarousel />
  </main>
</template>

<script>
import FreeLesson from "./FreeLesson.vue";
import Courses from "./Courses.vue";
import Referreal from "./Referreal.vue";
import Instructor from "./Instructor.vue";
import TestimonialCarousel from "./TestimonialCarousel.vue";

export default {
  components: {
    FreeLesson,
    Courses,
    Referreal,
    Instructor,
    TestimonialCarousel,
  },
};
</script>

<style>
</style>