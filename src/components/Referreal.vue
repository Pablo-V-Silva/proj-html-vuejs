<template>
  <div class="banner pt-5">
    <div class="container">
      <div class="row row-cols-3">
        <div class="col">
          <div class="card">
            <div class="circle-wrap position-relative mx-auto mt-4">
              <div class="innCircle"></div>
              <div
                class="
                  position-absolute
                  top-50
                  start-50
                  translate-middle
                  number
                "
              >
                95%
              </div>
              <div class="circle">
                <div class="left prog">
                  <div class="progressBar"></div>
                </div>
                <div class="right prog">
                  <div class="progressBar"></div>
                </div>
              </div>
            </div>
            <div class="inforate text-uppercase pt-5 pb-4 fs-3 text-center">
              pass rate
            </div>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <div class="circle-wrap position-relative mx-auto mt-4">
              <div class="innCircle"></div>
              <div
                class="
                  position-absolute
                  top-50
                  start-50
                  translate-middle
                  number
                "
              >
                100%
              </div>
              <div class="circle center">
                <div class="left prog">
                  <div class="progressBar"></div>
                </div>
                <div class="rightcenter prog">
                  <div class="progressBar"></div>
                </div>
              </div>
            </div>
            <div class="inforate text-uppercase pt-5 pb-4 fs-3 text-center">
              referreal rate
            </div>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <div class="circle-wrap position-relative mx-auto mt-4">
              <div class="innCircle"></div>
              <div
                class="
                  position-absolute
                  top-50
                  start-50
                  translate-middle
                  number
                "
              >
                1%
              </div>
              <div class="circle end">
                <div class="rightend prog">
                  <div class="progressBar"></div>
                </div>
              </div>
            </div>
            <div class="inforate text-uppercase pt-5 pb-4 fs-3 text-center">
              accident rate
            </div>
          </div>
        </div>
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

    .circle-wrap {
      width: 300px;
      height: 300px;
      border: 0px solid $principal_color;

      .innCircle {
        position: absolute;
        top: 50%;
        left: 50%;
        z-index: 6;
        width: 275px;
        height: 275px;
        background-color: white;
        border-radius: 50%;
        transform: translate(-50%, -50%);
      }

      .number {
        z-index: 7;
        font-size: 4rem;
      }

      .circle {
        .prog {
          width: 100%;
          height: 100%;
          background-color: white;
          position: absolute;
          border-radius: 50%;
          clip: rect(0, 300px, 300px, 150px);

          .progressBar {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            clip: rect(0, 150px, 300px, 0);
            background-color: $principal_color;
          }
        }

        .left .progressBar {
          z-index: 1;
          animation: left 1s linear both;
        }

        @keyframes left {
          100% {
            transform: rotate(180deg);
          }
        }

        .right {
          transform: rotate(180deg);
          z-index: 3;
        }

        .right .progressBar {
          animation: right 1s linear both;
          animation-delay: 1s;
        }
        @keyframes right {
          100% {
            transform: rotate(171deg);
          }
        }
      }
    }

    .center {
      .rightcenter {
        transform: rotate(180deg);
        z-index: 3;
      }
      .rightcenter .progressBar {
        animation: rightcenter 1s linear both;
        animation-delay: 1s;
      }
      @keyframes rightcenter {
        100% {
          transform: rotate(180deg);
        }
      }
    }

    .end {
      .rightend {
        z-index: 3;
      }
      .rightend .progressBar {
        animation: rightend 1s linear both;
        animation-delay: 1s;
      }
      @keyframes rightend {
        100% {
          transform: rotate(4deg);
        }
      }
    }
  }

  .inforate {
    color: $coursesTxt_color;
  }
}
</style>