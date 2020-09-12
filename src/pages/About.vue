<template>
  <Layout>
    <transition name="slide" appear>
      <grid />
    </transition>
  </Layout>
</template>

<script>
import grid from "../components/grid";

export default {
  components: { grid },
  metaInfo: {
    title: "About",
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.slide-enter-active {
  transition: opacity 0.5s;
  transition: transform 0.05s;
}

.slide-enter {
  opacity: 1;
  transform: translateX(1000px);
}

body {
  margin: 0;
  padding: 0;
}

.layout {
  padding: 0;
  overflow-x: hidden;
}
</style>
