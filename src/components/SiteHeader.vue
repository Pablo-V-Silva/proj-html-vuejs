<template>
  <header>
    <div class="contacts">
      <div class="container d-flex justify-content-between py-2">
        <div class="successfullRate">We have 95% Successful Pass Rate</div>
        <div class="greenNumber">
          <i class="fas fa-phone"></i>
          Give us a call to book your tuition! 1-800-555-555
        </div>
      </div>
    </div>
    <div class="jumbo">
      <div class="links">
        <nav class="navbar navbar-expand-lg navbar-dark">
          <div class="container py-3">
            <img src="../assets/img/avada-drivers-logo-1x.png" alt="" />
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#navbarNav"
              aria-controls="navbarNav"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
            <div
              class="collapse navbar-collapse justify-content-end"
              id="navbarNav"
            >
              <ul class="navbar-nav align-items-center">
                <li
                  class="nav-item d-flex align-items-center"
                  v-for="link in links"
                  :key="link.link"
                >
                  <a class="nav-link active" aria-current="page" href="#">{{
                    link.link.toUpperCase()
                  }}</a>
                  <span v-if="link.btn" class="newItem rounded-2">NEW</span>
                </li>
              </ul>
              <button type="button" class="btn rounded-pill greenBtn py-1">
                BOOK NOW
              </button>
            </div>
          </div>
        </nav>
      </div>

      <div class="vignet container">
        <h1 class="text-light">Drive width Avada</h1>
        <p class="text-light">
          We offer the finest driving tuition money can buy
        </p>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    links: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/variables.scss";

.contacts {
  background-color: $header_background;
  color: $headerUp_text;
  font-size: 0.8em;
}

.jumbo {
  background: url("../assets/img/homepage-hero-background.jpg");
  background-color: rgba(0, 0, 0, 0.42);
  background-blend-mode: multiply;
  background-repeat: no-repeat;
  background-size: cover;

  .links {
    background-color: rgba(0, 0, 0, 0.522);

    li {
      padding: 0 0.5rem;

      .newItem {
        background-color: $principal_color;
        color: white;
        font-size: 0.7em;
        padding: 3px 6px;
      }
    }
    .greenBtn {
      background-color: $principal_color;
      color: white;
      padding: 0.6rem 2rem;
    }
  }

  .vignet {
    padding: 9rem 0;
  }
}
</style>
