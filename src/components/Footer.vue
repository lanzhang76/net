<template>
  <div class="hover-footer">
    <div v-for="(i,key) in tags" :key="key">
      <span class="footer_tag">{{i.tag}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Foofoo",
  props: {},
  data() {
    return {
      tags: [
        { tag: "Python", display: "false" },
        { tag: "Javascript", display: "false" },
        { tag: "Machine Learning", display: "false" },
        { tag: "Vue.js", display: "false" },
        { tag: "HTML/CSS", display: "false" },
        { tag: "Unity", display: "false" },
        { tag: "C++", display: "false" },
        { tag: "OpenFrameworks", display: "false" },
        { tag: "Data Visualization", display: "false" },
        { tag: "Flask", display: "false" },
        { tag: "Natural Language Processing", display: "false" },
        { tag: "Performance Art", display: "false" },
        { tag: "Physical Computing", display: "false" },
        { tag: "Interaction Design", display: "false" }
      ]
    };
  }
};
</script>

<style scoped>
:root {
  --reg-font-size: 35px;
  --cap-font-size: 13px;
  --world-padding: 20px;
  --color-grey-base: #c0c0c0;
  --color-grey-highlight: #a9a9a9;
  --global-font-color: #333333;
}

.hover-footer {
  box-sizing: border-box;
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  padding: var(--world-padding);
  pointer-events: none;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap-reverse;
  align-items: center;
  font-size: var(--cap-font-size);
  color: var(--color-grey-base);
}

.footer_tag {
  padding-right: 10px;
  padding-top: 0;
}

@media only screen and (max-width: 600px) {
  .hover-footer {
    box-sizing: border-box;
    margin: 0;
    padding: 15px;
    font-size: 12px;
  }

  .footer_tag {
    padding: 0;
    padding-right: 10px;
  }
}
</style>