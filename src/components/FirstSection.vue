<template>
  <div class="freelesson container">
    <div class="row row-cols-1 row-cols-md-2">
      <div class="col py-5">
        <h2 class="text-capitalize title">get behind the wheel</h2>
        <p class="subTitle">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis,
          eius optio molestiae quibusdam dolores cum tempore facere voluptas
          beatae ad.ì
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          repellendus odit quo expedita ipsum ducimus in eum dolores
          consequuntur veniam. Nesciunt mollitia atque fugit voluptatum harum,
          porro commodi laudantium nostrum est similique quam a voluptatem odio,
          omnis, inventore nemo laborum!
        </p>
      </div>
      <div class="col card">
        <h3 class="text-capitalize text-center titleCard fs-1">
          first lesson free!
        </h3>
        <p class="text-center fs-5">
          When you make a block booking with us your fisrt lesson is includeed
          free
        </p>

        <form action="" class="px-3">
          <div class="name position-relative">
            <input
              type="text"
              name="name"
              id="name"
              placeholder="Your Name*"
              class="py-2 w-100 rounded"
            />
            <span><i class="far fa-id-badge icon"></i></span>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scope>
@import "../assets/scss/variables.scss";

.title {
  font-size: 2.9rem;
}

.subTitle {
  font-size: 1.2rem;
}

p {
  color: $headerUp_text;
}

.titleCard {
  color: $principal_color;
  padding: 2rem;
}

form {
  #name {
    border: 1px solid $headerUp_text;
    padding-left: 0.5rem;
  }

  .icon {
    position: absolute;
    right: 0.5rem;
    top: 50%;
    transform: translate(0, -50%);
    color: $headerUp_text;
  }
}
</style>