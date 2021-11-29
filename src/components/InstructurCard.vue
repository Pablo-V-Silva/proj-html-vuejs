<template>
  <div class="row row-cols-3 g-5 instructorsContain">
    <div class="col" v-for="instructor in instructors" :key="instructor.name">
      <div class="instructorCard">
        <div
          class="forBorder d-flex flex-column align-items-center"
          :class="instructor.center ? 'center' : ''"
        >
          <img
            :src="require(`../assets/img/${instructor.image}`)"
            alt=""
            width="80%"
            class="py-4"
          />
          <h4>{{ instructor.name }}</h4>
          <div class="social py-2">
            <i :class="instructor.firstsocial" class="px-2 fs-4"></i>
            <i :class="instructor.secondsocial" class="px-2 fs-4"></i>
            <i :class="instructor.thirdsocial" class="px-2 fs-4"></i>
          </div>
          <p class="mx-5 text-center">{{ instructor.speech }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      instructors: [
        {
          image: "instructor-mikehart.jpg",
          name: "Mike Hart",
          firstsocial: "fab fa-facebook-f",
          secondsocial: "fab fa-twitter",
          thirdsocial: "fab fa-instagram",
          speech: "Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          image: "instructor-johnsmith.jpg",
          name: "Jhon Smith",
          firstsocial: "fab fa-facebook-f",
          secondsocial: "fab fa-twitter",
          thirdsocial: "fab fa-instagram",
          speech: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          center: true,
        },
        {
          image: "instructor-angelahart.jpg",
          name: "Angela Hart",
          firstsocial: "fab fa-facebook-f",
          secondsocial: "fab fa-twitter",
          thirdsocial: "fab fa-instagram",
          speech: "Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/variables.scss";
.instructorsContain {
  position: absolute;

  .instructorCard {
    -webkit-box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
    box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
    min-height: 400px;
    border-top: 7px solid $principal_color;
    border-radius: 1rem;

    .forBorder {
      background-color: white;
      border-radius: 1rem;
      &.center {
        min-height: 420px;
      }
    }

    img {
      border-radius: 30px;
    }
    p,
    i {
      color: $coursesTxt_color;
    }

    i {
      cursor: pointer;

      &:hover {
        color: #5b7483;
      }
    }
  }
}
</style>