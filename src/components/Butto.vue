<template>
  <!-- <label>
      <input type="checkbox" />
      <span>{{title}}</span>
  </label>-->
  <a v-bind:href="info.link" target="_blank">
    <button class="ck-button">{{info.title}}</button>
  </a>
</template>

<script>
export default {
  name: "butto",
  props: { info: { title: "", link: "" } },
  data() {
    return {};
  }
};
</script>

<style scoped>
button {
  padding: 5px;
  background-color: none;
  border: 1px solid var(--global-font-color);
  margin-right: 5px;
  margin-bottom: 0;
  border-radius: 2px;
  float: left;
  font-size: var(--cap-font-size);
  color: var(--global-font-color);
  outline: none;
}

/* .ck-button {
  margin: 1px;
  border-radius: 2px;
  border: 1px solid royalblue;
  float: left;
  font-size: var(--cap-font-size);
} */

.ck-button:hover {
  animation: 1s grad forwards;
}

@keyframes grad {
  0% {
    background: white;
    color: black;
  }
  20% {
    background: royalblue;
    color: white;
  }
  100% {
    background: royalblue;
    color: white;
  }
}

/* .ck-button label span {
  text-align: center;
  padding: 5px;
  display: block;
}

.ck-button label input {
  position: absolute;
  top: -150px;
}

.ck-button input:checked + span {
  background-color: royalblue;
  color: #fff;
} */
</style>