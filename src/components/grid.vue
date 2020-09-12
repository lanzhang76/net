<template>
  <div class="wrapper">
    <div class="box vertical" id="half2">
      <div class="box horizontal">
        <div class="intro mobile-text">
          <h1>Hello there ✨ this is Lan.</h1>
          <br />I am a creative technologist, developer, and art director based in NYC. I enjoy making interactive tools related to language, graphics and play experiences on the web.
          <br />
          <br />I'm currently a freelance developer, an artist, and a part-time faculty at Parsons School of Design, where I received my MFA in Design and Technology.
        </div>
      </div>
      <div class="box horizontal" id="half4">
        <div class="box vertical email"></div>
        <div class="box vertical" id="half6">
          <div class="box horizontal">
            <div id="credits">
              <!-- <caption class="cap_small">Credit</caption> -->
              This site is built with
              <a href="https://vuejs.org/">Vue.js</a> and
              <a href="https://gridsome.org/">Gridsome</a>.
              Copyright © 2020 Lan Zhang
            </div>
            <div class="sketch">
              <iframe
                width="300px"
                height="210px"
                src="https://editor.p5js.org/lanzhang76/embed/Yz-EzEFfc"
              ></iframe>
            </div>
          </div>
          <div class="box horizontal" id="half8">
            <div class="box vertical">
              <div class="social-col mobile-text">
                <caption class="cap_small">Connect</caption>
                <!--  @click.native="showR" -->
                <butto v-bind:info="{title:`Email`,link:emailadd}" target="_top"></butto>
                <butto v-bind:info="{title:`Github`,link:git}"></butto>
                <butto v-bind:info="{title:`LinkedIn`,link:linkedin}"></butto>
                <butto v-bind:info="{title:`Instagram`,link:instagram}"></butto>
              </div>
            </div>
            <div class="box vertical" id="half10">
              <input type="checkbox" v-model="resume" />
              <caption class="cap_small">CV</caption>
              <h1 id="xmark" v-show="resume">✕</h1>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="box vertical">
      <resume v-show="resume" />
    </div>
  </div>
</template>

<script>
import resume from "../components/resume";
import butto from "../components/Butto";

export default {
  name: "grid",
  components: { resume, butto },
  data() {
    return {
      resume: false,
      cvLink: "/cv.pdf",
      resumeLink: "/lanzhangresume_ct.pdf",
      git: "https://github.com/lanzhang76",
      linkedin: "https://www.linkedin.com/in/lan-zhang-1700a0b0",
      instagram: "https://www.instagram.com/turniplan/",
      emailadd: "mailto:lan@lanzhang.net?Subject=Hello%20Lan",
    };
  },
};
</script>

<style scoped>
div {
  box-sizing: border-box;
}

.box {
  /* padding: 5px; */
  overflow-y: overlay;
}

.wrapper {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: row;
  background-color: #775dbf;
  font-size: 0.8em;
}

.vertical {
  height: 100%;
  width: 50%;
  flex-direction: row;
}

.horizontal {
  height: 50%;
  width: 100%;
  display: flex;
}
#half2 {
  background: #ffb200;
}

#half2,
#half2 a {
  color: #066f43;
}

#half4 {
  background-image: linear-gradient(#e88d39, #ef6969, #46c8c0, #c2d7ff);
}

#half6 {
  background: royalblue;
  float: right;
}

#half6,
#half6 a {
  color: #fff967;
}

#half8 {
  background: #f2f2f2;
  color: #434040;
}

#half10 {
  padding: 0;
  background-color: #434040;
  float: right;
  color: honeydew;
  position: relative;
  /* overflow: hidden; */
}

#half10 > caption {
  z-index: 2;
  position: absolute;
  padding: 10px;
}
#half10 > input {
  width: 100%;
  height: 100%;
  margin: 0;
  z-index: 0;
  position: absolute;
  -webkit-appearance: none;
  -moz-appearance: none;
  -o-appearance: none;
  appearance: none;
  outline: none;
}

#half10:hover {
  transition-duration: 0.2s;
  color: royalblue;
}
#half10 > input:hover {
  transition-duration: 0.6s;
  background-color: tomato;
  border: 5px solid royalblue;
}

#xmark {
  transition-duration: 0.2s;
  position: absolute;
  right: 10px;
  bottom: 0;
  pointer-events: none;
}

::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: transparent;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #c4c4c4;
}

p {
  margin: 0;
}

a {
  text-decoration: none;
  color: var(--global-font-color);
}

a:hover {
  color: darkgray;
}

h1 {
  margin: 0;
}

.intro {
  padding: 1em;
}

.email {
  padding: 0.5em;
}

#credits {
  font-size: 0.8em;
  padding: 10px;
}

.social-col {
  font-size: 0.8em;
  padding: 10px;
}

iframe {
  border: none;
}

.sketch {
  margin-top: -20px;
  position: absolute;
  z-index: 200;
  transition: opacity 2.5s;
}

@media only screen and (max-width: 600px) {
  .intro h1 {
    line-height: 1em;
  }

  .intro,
  .social-col {
    padding: 1em;
  }

  .box {
    padding: 0px;
    margin: 0px;
  }

  .wrapper {
    width: 100vw;
    height: auto;
    display: flex;
    flex-direction: column;
  }

  .horizontal,
  .vertical {
    display: flex;
    width: 100%;
    height: auto;
    flex-direction: column;
  }

  #half2 {
    order: -1;
  }

  .mobile-text {
    margin: 0em;
  }

  #half10 > caption {
    position: relative;
    padding: 1em;
    z-index: 0;
  }
  #half10 > input {
    width: 100%;
    height: 100%;
    z-index: 2;
  }

  #half6 {
    height: 10em;
  }

  #half10 > input:hover {
    transition-duration: 0s;
    background-color: transparent;
    border: 0px;
  }

  #xmark {
    display: none;
  }
}
</style>