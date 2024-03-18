<template>
  <header class="header">
    <div class="container">
      <div class="header--wrap">
        <a href="#" class="header-logo" title="PhotoFox">
          <img src="@/assets/images/svg/logo.svg" alt="PhotoFox" />
        </a>
        <vNavbar />
        <a href="#" class="header-btn btn btn--sm btn--thirdary" title="Go to Contact section">
          Contact
          <vButtonIcon />
        </a>
      </div>
    </div>
  </header>
</template>

<script>
import vButtonIcon from "@/components/vButtonIcon.vue";
import vNavbar from "./vNavbar.vue";

export default {
  components: {
    vButtonIcon,
    vNavbar,
  },
};
</script>
