<template>
  <g-link class="nav__link x" to="/">✕</g-link>
</template>

<script>
export default {
  name: "exit"
};
</script>

<style scoped>
.x {
  position: fixed;
  top: 0;
  right: 0;
  padding: var(--world-padding);
  font-size: 1rem;
}

.nav__link {
  /* margin-left: 20px; */
  text-decoration: none;
  color: #333333;
}

@media only screen and (max-width: 750px) {
  .x {
    position: fixed;
    top: 0;
    right: 0;
  }
}
</style>