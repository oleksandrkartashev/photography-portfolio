<template>
  <div class="welcome">
    <div class="welcome-image">
      <img src="@/assets/images/welcome/welcome-main.jpg" alt="PHOTOGRAPHER BRUCE WAYNE" />
      <div class="welcome-content">
        <h1>BRUCE WAYNE</h1>
        <p>PHOTOGRAPHER</p>
      </div>
    </div>

    <div class="welcome-carousel carousel">
      <carousel :items-to-show="3.5">
        <slide v-for="slide in slides" :key="slide.id">
          <figure class="carousel-item">
            <img
              :src="require('@/assets/images/welcome/carousel/' + slide.image)"
              :alt="slide.title"
            />
          </figure>
        </slide>
        <template #addons>
          <navigation />
        </template>
      </carousel>
    </div>
  </div>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Navigation } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
    Navigation,
  },
  data() {
    return {
      slides: [
        {
          id: 1,
          title: "jaguar-in-tropical-rainforest-at-night",
          image: "jaguar-in-tropical-rainforest-at-night.jpg",
        },
        {
          id: 2,
          title: "leopard-in-the-wild-national-park-kenya",
          image: "leopard-in-the-wild-national-park-kenya.jpg",
        },
        {
          id: 3,
          title: "lion-couple-laying-in-the-grass",
          image: "lion-couple-laying-in-the-grass.jpg",
        },
        {
          id: 4,
          title: "portrait-of-a-siberian-tiger",
          image: "portrait-of-a-siberian-tiger.jpg",
        },
        {
          id: 5,
          title: "jaguar-in-tropical-rainforest-at-night",
          image: "jaguar-in-tropical-rainforest-at-night.jpg",
        },
        {
          id: 6,
          title: "leopard-in-the-wild-national-park-kenya",
          image: "leopard-in-the-wild-national-park-kenya.jpg",
        },
        {
          id: 7,
          title: "lion-couple-laying-in-the-grass",
          image: "lion-couple-laying-in-the-grass.jpg",
        },
        {
          id: 8,
          title: "portrait-of-a-siberian-tiger",
          image: "portrait-of-a-siberian-tiger.jpg",
        },
      ],
    };
  },
};
</script>
