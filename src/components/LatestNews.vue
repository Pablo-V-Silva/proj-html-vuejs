<template>
  <div class="latestBanner position-relative">
    <div class="container forPosition">
      <div class="latestNewsContainer text-center">
        <h3 class="text-capitalize pt-5 pb-4 fs-1">latest news</h3>
        <div class="row row-cols-2 g-4">
          <div
            class="col mb-5"
            v-for="article in articles"
            :key="article.image"
          >
            <img
              :src="require(`../assets/img/${article.image}`)"
              alt=""
              width="100%"
              class="pb-3"
            />
            <h4 class="text-capitalize principalText">{{ article.title }}</h4>

            <p>
              {{ article.date }} |
              <span class="principalText">0 comments</span>
            </p>
            <p>{{ article.speech }}</p>
          </div>
        </div>
        <button class="mainBtn rounded-pill text-uppercase">
          more from the blog
        </button>
      </div>
      <img src="../assets/img/latestnews-bottom.png" alt="" width="100%" />
    </div>
  </div>
</template>

<script>
import dayjs from "../../node_modules/dayjs";
export default {
  data() {
    return {
      articles: [
        {
          image: "blog-choosecar-700x441.jpg",
          title: "what car to start with?",
          date: dayjs().format("MMMM Do, YYYY"),
          speech: "Lorem ipsum dolor sit amet consectetur adipisicing.",
        },
        {
          image: "blogpost-10and2-700x441.jpg",
          title: "avada driving school expanding",
          date: dayjs().format("MMMM Do, YYYY"),
          speech: "Lorem ipsum dolor sit amet consectetur adipisicing.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.latestBanner {
  position: relative;
  z-index: -1;
  background-image: url("../assets/img/latestnews-background.jpg");
  padding: 27rem 0;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;

  .forPosition {
    position: absolute;
    top: -2rem;
    left: 50%;
    transform: translate(-50%, 0);

    .latestNewsContainer {
      background-color: white;
      -webkit-box-shadow: 0px -5px 0px 0px #333333;
      -moz-box-shadow: 0px -5px 0px 0px #333333;
      -o-box-shadow: 0px -5px 0px 0px #333333;
      box-shadow: 0px -5px 0px 0px #333333;
      border-top-left-radius: 7px;
      border-top-right-radius: 7px;

      .row {
        margin: 0 4rem;
        .principalText {
          color: $principal_color;
        }
        p {
          color: $coursesTxt_color;
        }
      }
    }
  }
}
</style>