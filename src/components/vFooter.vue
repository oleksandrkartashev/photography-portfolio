<template>
  <footer class="footer">
    <div class="container">
      <div class="footer--wrap">
        <a href="#" class="footer-logo" title="PhotoFox">
          <img src="@/assets/images/svg/logo.svg" alt="PhotoFox" />
        </a>
        <nav class="footer-nav nav">
          <ul class="nav-list">
            <li class="nav-item" v-for="item in footerNavItems" :key="item.id">
              <a :href="item.link" class="nav-link" :title="item.title">{{ item.name }}</a>
            </li>
          </ul>
        </nav>
        <a href="#" class="footer-privacy" title="Go to Privacy page"> All right reserved </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      footerNavItems: [
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
    };
  },
};
</script>
