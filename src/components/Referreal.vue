<template>
  <div class="banner pt-5">
    <div class="container">
      <div class="row row-cols-3">
        <div class="col">
          <div class="card">
            <div class="circle-wrap d-flex justify-content-center pt-3">
              <div class="circlEst">
                <div class="circle">
                  <div
                    class="
                      number
                      d-flex
                      justify-content-center
                      align-items-center
                      h-100
                    "
                  >
                    95%
                  </div>
                </div>
              </div>
            </div>
            <div class="inforate text-uppercase pt-5 fs-3 text-center">
              pass rate
            </div>
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
@import "../assets/scss/variables.scss";

.banner {
  .card {
    -webkit-box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
    box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
    .circlEst {
      width: 300px;
      height: 300px;
      border-radius: 50%;
      background-color: $principal_color;
      display: flex;
      justify-content: center;
      align-items: center;

      .circle {
        background-color: white;
        width: 280px;
        height: 280px;
        border-radius: 50%;

        .number {
          font-size: 5rem;
          color: $coursesTxt_color;
        }
      }
    }
  }

  .inforate {
    color: $coursesTxt_color;
  }
}
</style>