<template>
  <div class="contactsFooter">
    <div class="container pb-5">
      <div class="row row-cols-4 g-5">
        <div class="col">
          <img src="../assets/img/avada-drivers-logo-1x.png" alt="" />
          <p class="pt-3 footerText">
            Avada Driving School is the right choice for experience drivers
            looking for a refresher course, or the brand new driver wanting to
            pass first time
          </p>
        </div>
        <div class="col">
          <h4 class="text-uppercase text-light">contacts details</h4>
          <ul>
            <li v-for="contact in contacts" :key="contact.text" class="py-2">
              <div
                class="contactText d-flex"
                :class="contact.uppercase ? 'text-capitalize' : ''"
              >
                <i :class="contact.icon" class="pe-3 pt-1 footerText"></i>
                <div class="text footerText">
                  <a href="" class="footerText">{{ contact.text }}</a>
                </div>
              </div>
            </li>
          </ul>
        </div>
        <div class="col">
          <h4 class="text-uppercase text-light">courses</h4>
          <ul>
            <li v-for="course in courses" :key="course.text" class="py-2">
              <div class="contactText principalText">
                <i :class="course.icon" class="pe-3"></i>
                <a href="" class="principalText">{{ course.text }}</a>
              </div>
            </li>
          </ul>
        </div>
        <div class="col text-center">
          <img src="../assets/img/footer-ad-grid.png" alt="" width="100%" />
          <button class="mainBtn rounded-pill text-center mt-4 text-uppercase">
            book now
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contacts: [
        {
          icon: "fas fa-home",
          text: "12345 north main street, new york nY 555555",
          uppercase: true,
        },
        {
          icon: "fas fa-phone",
          text: "1.800.555.6789",
          uppercase: true,
        },
        {
          icon: "fas fa-envelope",
          text: "info@your-demain.com",
        },
        {
          icon: "fas fa-link",
          text: "Theme-Fusion.com",
          uppercase: true,
        },
      ],
      courses: [
        {
          icon: "far fa-arrow-alt-circle-right",
          text: "Pass Plus",
        },
        {
          icon: "far fa-arrow-alt-circle-right",
          text: "Intensive Course",
        },
        {
          icon: "far fa-arrow-alt-circle-right",
          text: "Automatic",
        },
        {
          icon: "far fa-arrow-alt-circle-right",
          text: "Instructor Training",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.contactsFooter {
  background-image: url("../assets/img/footer-background-color.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  a {
    text-decoration: none;
  }
  .footerText {
    color: rgb(190, 190, 190);
  }
  .principalText {
    color: $coursesTxt_color;
  }

  ul {
    list-style: none;
    padding: 0;
  }
}
</style>