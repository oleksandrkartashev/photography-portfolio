<template>
  <nav class="header-nav nav">
    <ul class="nav-list" :class="{ 'nav-list--active': showNavbar }">
      <li class="nav-item" v-for="item in navbarItems" :key="item.id">
        <a :href="item.link" class="nav-link" :title="item.title">{{ item.name }}</a>
      </li>
    </ul>
    <button
      class="nav-btn btn--toggle"
      v-if="isMobile"
      @click="openNavbar"
      :class="{ 'btn--toggle--active': showNavbar }"
    >
      <i></i>
    </button>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      navbarItems: [
        {
          id: 1,
          name: "Home",
          title: "Go to Home page",
          link: "#",
        },
        {
          id: 2,
          name: "About",
          title: "Go to Home page",
          link: "#",
        },
        {
          id: 3,
          name: "Works",
          title: "Go to Works page",
          link: "#",
        },
      ],
      windowWidth: window.innerWidth,
      showNavbar: false,
    };
  },
  computed: {
    isMobile() {
      return this.windowWidth < 768;
    },
  },
  mounted() {
    window.addEventListener("resize", this.updateWindowWidth);
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.updateWindowWidth);
  },
  methods: {
    updateWindowWidth() {
      this.windowWidth = window.innerWidth;
    },
    openNavbar() {
      this.showNavbar = !this.showNavbar;
    },
  },
};
</script>
