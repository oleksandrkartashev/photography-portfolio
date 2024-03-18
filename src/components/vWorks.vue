<template>
  <div class="works">
    <div class="container">
      <h2 class="works-title">Selected works</h2>
      <ul v-if="works.length" class="works-masonry masonry">
        <li v-for="item in works" :key="item.id" class="masonry-item">
          <figure>
            <img :src="require('@/assets/images/works/' + item.image)" :alt="item.title" />
            <figcaption>{{ item.title }}</figcaption>
          </figure>
        </li>
      </ul>
      <div class="works--wrap">
        <a href="#" class="btn btn--lg btn--secondary">
          See all works
          <vButtonIcon />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import vButtonIcon from "./vButtonIcon.vue";

export default {
  components: {
    vButtonIcon,
  },
  data() {
    return {
      works: [
        {
          id: 1,
          title: "downtown-dubai-at-dawn-united-arab-emirates",
          image: "work1.jpg",
        },
        {
          id: 2,
          title: "roe-deer-portrait-in-the-winter-forest",
          image: "work2.jpg",
        },
        {
          id: 3,
          title: "little-girl-having-fun-with-drinking-water-at-stre",
          image: "work3.jpg",
        },
        {
          id: 4,
          title: "greenland-natura-landscape",
          image: "work4.jpg",
        },
        {
          id: 5,
          title: "lit-up-dome-tent-aurora-borealis-in-background",
          image: "work5.jpg",
        },
        {
          id: 6,
          title: "a-little-orange-bug-on-a-flower",
          image: "work6.jpg",
        },
        {
          id: 7,
          title: "baby-birds",
          image: "work7.jpg",
        },
        {
          id: 8,
          title: "a-side-profile-of-a-leopard-s-head",
          image: "work8.jpg",
        },
        {
          id: 9,
          title: "top-aerial-view-of-famous-snake-road-near-passo",
          image: "work9.jpg",
        },
      ],
    };
  },
};
</script>
