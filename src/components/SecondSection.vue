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
    <div class="bannercouses">
      <div class="container">
        <div class="row">
          <div class="col-6">
            <div class="card position-relative text-center py-5">
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
          <div class="col-2"></div>
          <div class="col-2"></div>
          <div class="col-2"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.bannerlearning {
  background-image: url("../assets/img/horizontal-cta-background.jpg");
  background-size: cover;
  background-position: center;
  padding: 4rem 0;
}

.newCorner {
  position: absolute;
  top: 0;
  left: 0;
  width: 15%;
}
</style>