<template>
  <div class="emailBanner">
    <div class="contain w-50 mx-auto text-center">
      <h3 class="py-4">Sign up to our Newsletter</h3>
      <div class="form w-75 mx-auto">
        <input type="text" name="" id="" class="w-100 mb-4" />
        <button class="mainBtn w-100 rounded-pill text-uppercase mb-4">
          subscribe
        </button>
      </div>
      <p class="principalText">
        (We do not share your data with anybody,and only use it for its intended
        purpose)
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.emailBanner {
  background-image: url("../assets/img/newsletter_background.jpg");
  background-position: center;
  background-size: cover;
  padding: 3rem 0;
  margin-bottom: 3rem;

  .principalText {
    color: $coursesTxt_color;
  }
}
</style>