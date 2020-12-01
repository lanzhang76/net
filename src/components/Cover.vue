<template>
  <div class="post">
    <img v-bind:src="url" />
  </div>
</template>

<script>
export default {
  name: "cover",
  props: ["url"],
  data() {
    return {};
  }
};
</script>


<style scoped>
.post {
  background: white;
  width: 1000px;
  height: 600px;
  position: fixed;
  display: flex;
  /* top: 50%; */
  /* left: 50%; */
  /* transform: translate(-50%, -50%); */
  z-index: -5;
}

.post img {
  width: 1000px;
  height: 600px;
  object-fit: contain;
}

@media only screen and (max-width: 1000px) {
  .post {
    width: 100%;
  }

  .post img {
    width: 100%;
    height: auto;
  }
}
</style>