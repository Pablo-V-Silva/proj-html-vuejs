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
    <div class="jumbo position-relative">
      <img
        src="../assets/img/homepage-hero-background.jpg"
        alt=""
        width="100%"
        class="heroImage"
      />
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
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >HOME</a
                  >
                </li>
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >ABOUT</a
                  >
                </li>
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >PRICES</a
                  >
                </li>
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >COURSES</a
                  >
                  <!-- IMG DINAMICA -->
                </li>
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >LOCATION</a
                  >
                </li>
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >BLOG</a
                  >
                </li>
                <li class="">
                  <button type="button" class="btn rounded-pill greenBtn py-1">
                    BOOK NOW
                  </button>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/variables.scss";

.contacts {
  background-color: $header_background;
  color: $headerUp_text;
}

.jumbo {
  background-repeat: no-repeat;
  background-size: cover;

  .heroImage {
    position: absolute;
    z-index: -1;
    object-fit: contain;
    background: rgb(63, 94, 251);
    background: radial-gradient(
      circle,
      rgba(63, 94, 251, 0) 66%,
      rgba(0, 0, 0, 0.5270483193277311) 88%
    );
  }

  .links {
    background-color: rgba(0, 0, 0, 0.522);

    li {
      padding: 0 0.5rem;

      .greenBtn {
        background-color: $principal_color;
        color: white;
        padding: 0.6rem 2rem;
      }
    }
  }
}
</style>
