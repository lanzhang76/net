<template>
  <div class="layout">
    <header class="header">
      <div class="header_element header1">
        <g-link class="header_name" to="/">
          <!-- <div class="bar"></div> -->
          Lan Zhang
        </g-link>
      </div>
    </header>
    <slot />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Heebo:wght@100;300;400;500&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400&family=Rozha+One&display=swap");

:root {
  --reg-font-size: 25px;
  --big-font: 45px;
  --cap-font-size: 18px;
  --world-padding: 20px;
  --mobile-world-padding: 15px;
  --color-grey-base: #c0c0c0;
  --color-grey-highlight: #a9a9a9;
  --global-font-color: #333333;
  --top-sticky: 60px;
  --global-cap: 11px;
  --highlight-salmon: #ffb7b7;
  --highlight-blue: royalblue;
}

body {
  cursor: url("/cursor.png"), default;
  font-family: sans-serif;
  font-family: "Poppins", sans-serif;
  font-size: var(--reg-font-size);
  color: var(--global-font-color);
  margin: 0;
  padding: 0;
  word-spacing: 1px;
}

a:hover {
  cursor: url("/cursorh.png"), default;
}

::selection {
  background: #ffb7b7;
}
::-moz-selection {
  background: #ffb7b7;
}
.cap_small {
  font-size: var(--global-cap);
  padding-bottom: 12px;
  text-align: left;
}
.layout {
  margin: 0 auto;
  padding: var(--world-padding);
  font-size: 20px;
  font-weight: 300;
}

.header {
  position: fixed;
  display: inline-block;
  left: 0;
  bottom: 0;
  font-size: 25px;
  z-index: 100;
}

.header_element {
  padding: var(--world-padding);
}

.header1 {
  font-size: var(--reg-font-size);
}

.bar {
  display: inline-block;
  width: 13px;
  height: 13px;
  margin: -1px 10px 0 3px;
  background: royalblue;
  animation: spin 1s linear infinite;
  animation-play-state: paused;
}

.bar:hover {
  animation-play-state: running;
}

@keyframes spin {
  to {
    transform: rotate(1turn);
  }
}

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

.header_name {
  text-decoration: none;
  color: #333333;
  font-weight: 400;
}

@media only screen and (max-width: 1000px) {
  body {
  }

  .header {
    display: nowrap;
  }
  .header_element {
    z-index: 100;
  }

  .x {
    position: fixed;
    top: 0;
    right: 0;
  }
}
</style>
