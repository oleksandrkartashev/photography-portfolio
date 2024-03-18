<template>
  <div class="promo">
    <div class="container">
      <div class="promo--wrap">
        <h2 class="promo-title">
          Let’s do<br />
          something<br />
          amazing together!
        </h2>
        <a href="#" title="Work with me" class="promo-btn btn btn--lg btn--primary">
          Work with me
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
};
</script>
