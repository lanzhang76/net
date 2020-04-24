<template>
  <div class="updiv">
    <button v-on:click="topFunction()" id="myBtn">↑</button>
  </div>
</template>

<script>
export default {
  name: "scrollTop",
  methods: {
    topFunction: function() {
      document.body.scrollTop = 0; // For Safari
      document.documentElement.scrollTop = 0; // Chrome
    }
  }
};
</script>

<style scoped>
.updiv {
  position: fixed;
  bottom: 0;
  right: 0px;
  box-sizing: border-box;
  padding: var(--world-padding);
}

#myBtn {
  font-size: var(--reg-font-size);
  padding: 5px;
  z-index: 2;
  border: none;
  outline: none;
  background-color: none;
  color: #999999;
  cursor: pointer;
  font-weight: 300;
}

#myBtn:hover {
  animation: 1s grad forwards;
}

@keyframes grad {
  0% {
    color: var(--global-font-color);
  }
  100% {
    color: black;
  }
}
</style>