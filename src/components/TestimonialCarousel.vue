<template>
  <div class="carouselContain">
    <h2>Testimonials</h2>
    <p>Here's what our happy drivers had to say about our services:</p>

    <div class="carousel">
      <div id="active" class="d-flex flex-column align-items-center">
        <img
          :src="require(`../assets/img/${testimonials[counter].image}`)"
          alt=""
          width="160px"
          class="py-4"
        />
        <p class="w-50 speech">
          {{ testimonials[counter].speech }}
        </p>
        <p class="name">
          <strong>{{ testimonials[counter].name }}</strong>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      testimonials: [
        {
          image: "testimonial-sophia.png",
          speech: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. In officiis
        facere doloremque eaque natus, alias assumenda voluptates accusamus
        quibusdam corporis fugiat obcaecati, ullam molestiae consequatur minus
        dolorum laborum reprehenderit, ea exercitationem. Enim ut pariatur
        tempora necessitatibus ex maiores nulla mollitia?`,
          name: "Sophia Jones",
        },
        {
          image: "testimonial-kelly.png",
          speech: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. In officiis
        facere doloremque eaque natus, ea exercitationem. Enim ut pariatur
        tempora necessitatibus ex maiores nulla mollitia?`,
          name: "Kelly Brown",
        },
        {
          image: "testimonial-kate.png",
          speech: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. In officiis
        facere doloremque eaque natus, alias assumenda voluptates accusamus
        quibusdam corporis fugiat obcaecati, ullam molestiae consequatur minus
        dolorum laborum reprehenderit, ea exercitationem. Enim ut pariatur
        tempora necessitatibus ex maiores nulla mollitia?`,
          name: "Kate Miller",
        },
        {
          image: "testimonial-harold.png",
          speech: `Lorem ipsum dolor sit, alias assumenda voluptates accusamus
        quibusdam corporis fugiat obcaecati, ea exercitationem. Enim ut pariatur
        tempora necessitatibus ex maiores nulla mollitia?`,
          name: "Harold Rodriguez",
        },
        {
          image: "testimonial-grant.png",
          speech: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. In officiis
        facere doloremque eaque natus, alias assumenda voluptates accusamus
        quibusdam corporis fugiat obcaecati, ullam molestiae consequatur minus
        dolorum laborum reprehenderit, ea exercitationem.`,
          name: "Grant Walker",
        },
      ],
      counter: 0,
    };
  },
  mounted() {
    this.plusCounter();
  },
  methods: {
    plusCounter() {
      let active = document.getElementById("active");

      setTimeout(() => {
        active.classList.add("animation");
      }, 5 * 1000);

      setInterval(() => {
        setTimeout(() => {
          active.classList.add("animation");
        }, 5 * 1000);

        if (active.classList.contains("animation")) {
          active.classList.remove("animation");
        }

        if (this.counter == this.testimonials.length - 1) {
          this.counter = 0;
        } else {
          this.counter++;
        }
      }, 6 * 1000);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/variables.scss";

.carouselContain {
  background-image: url("../assets/img/testimonial-background.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  text-align: center;
  padding: 10rem 0 14rem;
  position: relative;
  top: 22rem;
  z-index: -3;

  p {
    color: $coursesTxt_color;
  }
  .carousel {
    #active {
      transition: all 1s;

      .speech {
        position: absolute;
        top: 13.5rem;
      }

      .name {
        position: absolute;
        bottom: -11rem;
      }
    }
    .animation {
      transition: all 1s;
      opacity: 0;
    }
    .testSelectDot {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background-color: black;
    }
  }
}
</style>