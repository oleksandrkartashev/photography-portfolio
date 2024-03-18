<template>
  <vHeader />
  <vWelcome />
  <vInfo />
  <vTopics />
  <vWorks />
  <vPromo />
  <vFooter />
</template>

<script>
import vHeader from "./components/vHeader.vue";
import vWelcome from "./components/vWelcome.vue";
import vInfo from "./components/vInfo.vue";
import vWorks from "./components/vWorks.vue";
import vPromo from "./components/vPromo.vue";
import vFooter from "./components/vFooter.vue";
import vTopics from "./components/vTopics.vue";

export default {
  components: {
    vHeader,
    vWelcome,
    vInfo,
    vPromo,
    vTopics,
    vWorks,
    vFooter,
  },
};
</script>
