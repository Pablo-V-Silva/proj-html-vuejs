<template>
  <div class="instructor">
    <div class="container">
      <div class="row">
        <div class="col-8">
          <h3 class="text-capitalize pb-5">your instructor</h3>
          <div class="lorem">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nobis
            distinctio illum nesciunt sint officiis recusandae eos iure ad, quas
            sapiente veritatis, modi alias molestias est tempore, quae iusto
            consectetur veniam.
          </div>
        </div>

        <div class="col-4 d-flex align-items-center">
          <button class="text-uppercase mainBtn rounded-pill w-100">
            more about us
          </button>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="row row-cols-3">
        <div class="col">
          <div class="card">
            <img src="" alt="" />
            <h4>nome</h4>
            <div class="social"></div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Non,
              quam.
            </p>
          </div>
        </div>
        <div class="col"></div>
        <div class="col"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.instructor {
  padding-top: 6rem;
  .col-8 {
    h3 {
      font-size: 3rem;
    }
    .lorem {
      padding-bottom: 6rem;
    }
  }
}
</style>