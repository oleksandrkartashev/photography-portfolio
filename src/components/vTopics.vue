<template>
  <div class="topics">
    <div class="container">
      <div class="topics--wrap">
        <div class="topics--column">
          <h2 class="topics-title">Experience of 10 years in the field</h2>
          <figure class="topics-image--main">
            <img
              src="@/assets/images/topics/topics-main.jpg"
              alt="Experience of 10 years in the field"
            />
          </figure>
        </div>
        <div class="topics--column">
          <div class="topics-content">
            <ul class="topics-list list">
              <li v-for="topic in topics" :key="topic.id" class="list-item">
                <a :href="topic.url" :title="topic.title">
                  {{ topic.title }}
                  <vTopicsIcon />
                </a>
              </li>
            </ul>
            <a href="#" title="Work with me" class="topics-btn btn btn--lg btn--primary">
              About me
              <vButtonIcon />
            </a>
          </div>
          <figure class="topics-image--secondary">
            <img src="@/assets/images/topics/topics-secondary.jpg" alt="Food" />
          </figure>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import vTopicsIcon from "./vTopicsIcon.vue";
import vButtonIcon from "./vButtonIcon.vue";

export default {
  components: {
    vTopicsIcon,
    vButtonIcon,
  },
  data() {
    return {
      topics: [
        { id: 1, title: "FOOD PHOTOGRAPHY", url: "#" },
        { id: 2, title: "PORTRAIT PHOTOGRAPHY", url: "#" },
        { id: 3, title: "ARCHITECTURE PHOTOGRAPHY", url: "#" },
        { id: 4, title: "CONCEPTUAL PHOTOGRAPHY", url: "#" },
      ],
    };
  },
};
</script>
