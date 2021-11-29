<template>
  <header>
    <!-- Numero verde -->
    <div class="contacts">
      <div class="container d-flex justify-content-between py-2">
        <div class="successfullRate">We have 95% Successful Pass Rate</div>
        <div class="greenNumber">
          <i class="fas fa-phone"></i>
          Give us a call to book your tuition! 1-800-555-555
        </div>
      </div>
    </div>

    <!-- immagine di sfondo jumbo -->
    <div class="jumbo">
      <!-- navbar dinamica -->
      <div class="links">
        <nav class="navbar navbar-expand-lg navbar-dark">
          <div class="container py-3">
            <!-- logo azienda -->
            <img src="../assets/img/avada-drivers-logo-1x.png" alt="" />

            <!-- hamburger-menu -->
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

            <!-- elementi della navbar -->
            <div
              class="collapse navbar-collapse justify-content-end"
              id="navbarNav"
            >
              <ul class="navbar-nav align-items-center">
                <!-- link in links / link.link elemento del nav -->
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

              <!-- ordinazione del libro di sicurezza alla guida -->
              <button type="button" class="rounded-pill mainBtn">
                BOOK NOW
              </button>
            </div>
          </div>
        </nav>
      </div>

      <!-- frase motivazionale dell'azienda -->
      <div class="vignet container">
        <h1 class="text-light h-title">Drive with Avada</h1>
        <p class="text-light h-paragrap fw-light">
          We offer the finest driving tuition money can buy
        </p>

        <!-- bottoni per la selezione dei servizi dell'azienda messi in position fixed per averci sempre accesso -->
        <div class="products">
          <div class="cardproduct">
            <img src="../assets/img/demoss.svg" alt="" class="bg-light" />
            <div class="">Demos</div>
          </div>
          <div class="cardproduct mt-2">
            <div class="green_text">
              <span class="costValue">$</span><span class="fs-4">39</span>
            </div>
            <div class="">On Sale</div>
          </div>
        </div>
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

      a:hover {
        color: greenyellow;
        border-bottom: 2px solid greenyellow;
      }
    }
  }

  .vignet {
    padding: 9rem 0;

    .h-title {
      font-size: 3.5rem;
    }

    .h-paragrap {
      font-size: 1.5rem;
    }

    .products {
      position: fixed;
      right: 1rem;
      top: 7.7rem;
      z-index: 20;

      .cardproduct {
        width: 65px;
        padding: 0.3em;
        background: white;
        text-align: center;
        border-radius: 5px;

        .green_text {
          color: $principal_color;

          .costValue {
            position: relative;
            bottom: 0.5em;
          }
        }
      }
    }
  }
}
</style>
