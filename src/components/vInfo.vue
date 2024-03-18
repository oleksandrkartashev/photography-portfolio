<template>
  <div class="info">
    <div class="container">
      <div class="info--wrap">
        <span v-for="item in infoItems" :key="item">{{ item }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      infoItems: ["BASED IN GOTHAM", "AVAILABLE WORLDWIDE", "UTC+7"],
    };
  },
};
</script>
