<template>
  <Layout>
    <div class="parent-col">
      <div class="left-col">
        <div class="left-sec">
          <caption class="cap_small">Download/View</caption>
          <!--  @click.native="showR" -->
          <butto v-bind:info="{title:`CV`,link:cvLink}"></butto>
          <butto v-bind:info="{title:`Resume`,link:resumeLink}"></butto>
        </div>
        <div class="left-sec" id="connect_buttons">
          <caption class="cap_small">Connect</caption>
          <!--  @click.native="showR" -->
          <butto v-bind:info="{title:`Git`,link:git}"></butto>
          <butto v-bind:info="{title:`LinkedIn`,link:linkedin}"></butto>
        </div>
      </div>
      <div class="right-col">
        <p class="intro">
          Hello there, this is Lan.
          <br />
          <br />I am a developer and designer based in New York City.
          <br />I hold an MFA in
          <a
            href="https://www.newschool.edu/parsons/mfa-design-technology/"
            target="_blank"
          >Design and Technology</a> from Parsons School of Design. I am a
          <a
            href="https://www.recurse.com/"
            target="_blank"
          >Recurse Center</a> Winter2'20 alum.
          I worked as an art director at
          <a
            href="https://www.publicisna.com/"
            target="_blank"
          >Publicis NY</a>. Before that, I studied Advertising and Psychology at Syracuse University.
          <br />
          <br />Say hi at
          <a
            href="mailto:lan@lanzhang.net?Subject=Hello%20Lan"
            target="_top"
            style="text-decoration: underline"
          >Lan@Lanzhang.net</a>
        </p>
        <br />

        <div v-show="resume">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. In est ante in nibh. Sed augue lacus viverra vitae congue eu consequat ac. Venenatis tellus in metus vulputate eu scelerisque. Non blandit massa enim nec. Eu facilisis sed odio morbi. Egestas congue quisque egestas diam. Nunc scelerisque viverra mauris in aliquam sem fringilla. Elit pellentesque habitant morbi tristique. Eget dolor morbi non arcu.
            Amet justo donec enim diam vulputate ut. Risus nullam eget felis eget. Cursus eget nunc scelerisque viverra mauris in aliquam sem. Ut porttitor leo a diam sollicitudin tempor. Pellentesque sit amet porttitor eget dolor morbi non arcu. Ornare aenean euismod elementum nisi quis eleifend. Non nisi est sit amet facilisis magna etiam tempor. In massa tempor nec feugiat nisl. Massa tincidunt dui ut ornare lectus sit amet est. Malesuada fames ac turpis egestas maecenas.
            Quis vel eros donec ac odio. Elementum curabitur vitae nunc sed velit dignissim sodales ut eu. Donec ultrices tincidunt arcu non sodales neque sodales ut. Ut aliquam purus sit amet luctus. Leo a diam sollicitudin tempor id eu nisl nunc. Gravida dictum fusce ut placerat orci nulla pellentesque. Cras ornare arcu dui vivamus arcu felis bibendum ut tristique. Consectetur adipiscing elit pellentesque habitant. Dui ut ornare lectus sit. Nec sagittis aliquam malesuada bibendum arcu. Odio ut enim blandit volutpat maecenas volutpat. Enim sed faucibus turpis in eu mi.
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. In est ante in nibh. Sed augue lacus viverra vitae congue eu consequat ac. Venenatis tellus in metus vulputate eu scelerisque. Non blandit massa enim nec. Eu facilisis sed odio morbi. Egestas congue quisque egestas diam. Nunc scelerisque viverra mauris in aliquam sem fringilla. Elit pellentesque habitant morbi tristique. Eget dolor morbi non arcu.
            Amet justo donec enim diam vulputate ut. Risus nullam eget felis eget. Cursus eget nunc scelerisque viverra mauris in aliquam sem. Ut porttitor leo a diam sollicitudin tempor. Pellentesque sit amet porttitor eget dolor morbi non arcu. Ornare aenean euismod elementum nisi quis eleifend. Non nisi est sit amet facilisis magna etiam tempor. In massa tempor nec feugiat nisl. Massa tincidunt dui ut ornare lectus sit amet est. Malesuada fames ac turpis egestas maecenas.
            Quis vel eros donec ac odio. Elementum curabitur vitae nunc sed velit dignissim sodales ut eu. Donec ultrices tincidunt arcu non sodales neque sodales ut. Ut aliquam purus sit amet luctus. Leo a diam sollicitudin tempor id eu nisl nunc. Gravida dictum fusce ut placerat orci nulla pellentesque. Cras ornare arcu dui vivamus arcu felis bibendum ut tristique. Consectetur adipiscing elit pellentesque habitant. Dui ut ornare lectus sit. Nec sagittis aliquam malesuada bibendum arcu. Odio ut enim blandit volutpat maecenas volutpat. Enim sed faucibus turpis in eu mi.
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. In est ante in nibh. Sed augue lacus viverra vitae congue eu consequat ac. Venenatis tellus in metus vulputate eu scelerisque. Non blandit massa enim nec. Eu facilisis sed odio morbi. Egestas congue quisque egestas diam. Nunc scelerisque viverra mauris in aliquam sem fringilla. Elit pellentesque habitant morbi tristique. Eget dolor morbi non arcu.
            Amet justo donec enim diam vulputate ut. Risus nullam eget felis eget. Cursus eget nunc scelerisque viverra mauris in aliquam sem. Ut porttitor leo a diam sollicitudin tempor. Pellentesque sit amet porttitor eget dolor morbi non arcu. Ornare aenean euismod elementum nisi quis eleifend. Non nisi est sit amet facilisis magna etiam tempor. In massa tempor nec feugiat nisl. Massa tincidunt dui ut ornare lectus sit amet est. Malesuada fames ac turpis egestas maecenas.
            Quis vel eros donec ac odio. Elementum curabitur vitae nunc sed velit dignissim sodales ut eu. Donec ultrices tincidunt arcu non sodales neque sodales ut. Ut aliquam purus sit amet luctus. Leo a diam sollicitudin tempor id eu nisl nunc. Gravida dictum fusce ut placerat orci nulla pellentesque. Cras ornare arcu dui vivamus arcu felis bibendum ut tristique. Consectetur adipiscing elit pellentesque habitant. Dui ut ornare lectus sit. Nec sagittis aliquam malesuada bibendum arcu. Odio ut enim blandit volutpat maecenas volutpat. Enim sed faucibus turpis in eu mi.
          </p>
        </div>
      </div>
      <div class="social-col"></div>
      <scrollTop v-show="resume" />
    </div>
    <div id="credits">
      This site is built with
      <a href="https://vuejs.org/">Vue.js</a> and
      <a href="https://gridsome.org/">Gridsome</a>.
      Copyright © 2020 Lan Zhang
    </div>
  </Layout>
</template>

<script>
import scrollTop from "../components/scrollTop";
import exit from "../components/Exit";
import butto from "../components/Butto";

export default {
  components: { scrollTop, exit, butto },
  metaInfo: {
    title: "About"
  },
  data() {
    return {
      resume: false,
      cvLink: "/cv.pdf",
      resumeLink: "/resumeweb.pdf",
      git: "https://github.com/lanzhang76",
      linkedin: "https://www.linkedin.com/in/lan-zhang-1700a0b0"
    };
  },
  methods: {
    showR: function() {
      if (this.resume == false) {
        this.resume = true;
      } else {
        this.resume = false;
      }
      console.log(this.resume);
    }
  }
};
</script>

<style scoped>
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

.cap_small {
  font-size: var(--global-cap);
  padding-bottom: 12px;
  text-align: left;
}

.left-col {
  display: flex;
  flex-flow: column;
}

.left-sec {
  margin-bottom: 50px;
}

#connect_buttons {
  display: none;
}

#credits {
  position: fixed;
  right: 0;
  bottom: 0;
  padding: var(--world-padding);
  font-size: 13px;
}

@media only screen and (min-width: 1000px) {
  .parent-col {
    display: flex;
    font-size: var(--reg-font-size);
  }

  .left-col {
    flex-basis: 300px;
  }

  .right-col {
    flex-basis: calc(100%-600px);
    right: 300px;
    width: 800px;
  }

  .social-col {
    flex-basis: 150px;
    right: 0;
  }
}
@media only screen and (max-width: 1000px) {
  .parent-col {
    display: flex;
    flex-direction: column;
  }

  .left-col {
    position: relative;
    display: flex;
    flex-flow: row;
    width: 100%;
    margin-bottom: 2rem;
    justify-content: space-between;
    order: 1;
  }

  .right-col {
    order: 2;
    position: relative;
    margin-left: 0;
    width: 100%;
  }
  #credits {
    position: relative;
    padding: 0;
  }
}
</style>
