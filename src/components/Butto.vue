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
  },
};
</script>

<style scoped>
button {
  padding: 2px 5px 2px 5px;
  background-color: #775dbf;
  border: 3px solid #5e8de8;
  margin-right: 5px;
  margin-bottom: 5px;
  border-radius: 5px;
  float: left;
  font-size: var(--cap-font-size);
  color: white;
  outline: none;
  font-size: 1em;
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
    background: black;
    color: black;
  }
  20% {
    background: #5e8de8;
    color: white;
  }
  100% {
    background: #5e8de8;
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