<template>
  <div class="freelesson container">
    <div class="row row-cols-1 row-cols-md-2">
      <div class="col py-5 d-flex flex-column justify-content-center">
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
      <div class="col position-relative">
        <div class="card px-5">
          <h3 class="text-capitalize text-center titleCard fs-2">
            first lesson free!
          </h3>
          <p class="text-center pb-4">
            When you make a block booking with us your fisrt lesson is includeed
            free
          </p>

          <form action="" class="">
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
            <input
              type="email"
              name="email"
              id="email"
              placeholder="Your email"
              class="py-2 w-100 rounded"
            />
            <input
              type="text"
              name="telephone"
              id="telephone"
              placeholder="Your Telephone"
              class="py-2 w-100 rounded"
            />
            <input
              type="text"
              name="location"
              id="location"
              placeholder="Your Location"
              class="py-2 w-100 rounded"
            />
            <div class="text-center mb-3 mt-4">
              <button class="mainBtn rounded-pill text-uppercase">
                request a callback
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss" scope>
@import "../assets/scss/variables.scss";

.freelesson.container {
  padding: 5rem 0;
}
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

.card {
  margin: 0 4.5rem;
  position: absolute;
  top: -7.5rem;
  -webkit-box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);
  box-shadow: 0px 30px 50px 14px rgba(0, 0, 0, 0.4);

  form {
    padding-bottom: 1.5rem;

    #name,
    #email,
    #telephone,
    #location {
      border: 1px solid $headerUp_text;
      padding-left: 0.5rem;
      margin-bottom: 0.7rem;
      background-color: rgba(212, 212, 212, 0.438);
    }

    .icon {
      position: absolute;
      right: 0.5rem;
      top: 44%;
      transform: translate(0, -50%);
      color: $headerUp_text;
    }
  }
}
</style>