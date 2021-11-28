<template>
  <div>
    <div class="bannerlearning">
      <div class="container">
        <div class="row row-cols-2">
          <div class="col">
            <h3 class="text-capitalize text-light">
              start learning <span class="text-lowercase">to</span> drive today
            </h3>
            <div class="text-light">
              Give us a call to schedule your first driving lessons
            </div>
          </div>
          <div class="col d-flex justify-content-center align-items-center">
            <div class="text-light fs-2">
              <i class="fas fa-phone me-3"></i> 1-800-555-555
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bannercourses position-relative">
      <div class="container">
        <div class="row">
          <div class="col-6">
            <div class="infocourse">
              <div class="card position-relative text-center py-5 mx-5">
                <img
                  class="newCorner"
                  src="../assets/img/new-corner.jpg"
                  alt=""
                />
                <h3>Courses</h3>
                <div class="text pt-4 pb-5 px-5">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex
                  molestias adipisci eveniet aperiam sequi, voluptatibus,
                  quibusdam architecto id vero odit perferendis animi similique
                  dolores recusandae, praesentium suscipit beatae. Cupiditate,
                  labore?
                </div>
                <button class="mainBtn text-uppercase rounded-pill mx-auto">
                  course information
                </button>
              </div>
            </div>
          </div>
          <div class="col-6 d-flex align-items-center">
            <CardCar :courses="coursesArr" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardCar from "./CardCar.vue";
export default {
  components: {
    CardCar,
  },
  data() {
    return {
      coursesArr: [
        {
          img: "courses-passplus.jpg",
          title: "Pass Plus",
          ctaInfo: "Learn More",
        },
        {
          img: "course-intensive.jpg",
          title: "Intensive Course",
          ctaInfo: "Learn More",
        },
        {
          img: "courses-instructor.jpg",
          title: "Instructor",
          ctaInfo: "Learn More",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/variables.scss";

.bannerlearning {
  background-image: url("../assets/img/horizontal-cta-background.jpg");
  background-size: cover;
  background-position: center;
  padding: 4.8rem 0;
}

.newCorner {
  position: absolute;
  top: 0;
  left: 0;
  width: 15%;
  border-top-left-radius: 5px;
}

.bannercourses {
  background-image: url("../assets/img/promise-background.jpg");
  background-size: cover;
  padding: 5rem 0 6.3rem 0;
  background-position: bottom;
  background-repeat: no-repeat;
  background-blend-mode: multiply;
  background-color: $courses_bg;

  .infocourse {
    position: absolute;
    top: -2rem;
    width: calc(100% / 2.9);

    .card {
      position: relative;
      display: flex;
      flex-direction: column;
      min-width: 0;
      word-wrap: break-word;
      background-color: #fff;
      background-clip: border-box;
      border: 1px solid rgba(0, 0, 0, 0.125);
      border-radius: 0.25rem;
      -webkit-box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
      box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
    }
  }
}
</style>