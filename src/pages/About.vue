<template>
  <Layout>
    <div class="parent-col">
      <div class="left-col">
        <div>
          <caption class="cap_small">Download/View</caption>

          <butto @click.native="showR" v-bind:title="`CV`"></butto>
          <butto v-bind:title="`Resume`"></butto>
        </div>
      </div>
      <div class="right-col">
        <p class="intro">
          Hello there, this is Lan.
          <br />
          <br />I am a creative developer and designer.
          <br />I'm currently a MFA candidate at Design and Technology program at Parsons School of Design in NYC.
          I worked professionally as an art director in the advertising industry. Before that, I studied Advertising and Psychology at Syracuse University.
          <br />
          <br />You can say hi to me at 📨
          <a
            href="mailto:lanzhangwork@gmail.com?Subject=Hello%20Lan"
            target="_top"
          >lanzhangwork@gmail.com</a>
        </p>
        <br />
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
      <scrollTop v-show="resume" />
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
      resume: false
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

@media only screen and (min-width: 1000px) {
  .parent-col {
    display: flex;
    font-size: var(--reg-font-size);
  }

  .left-col {
    position: -webkit-sticky;
    position: sticky;
    height: 100%;
    flex-basis: 300px;
  }

  .right-col {
    flex-basis: calc(100%-300px);
    right: 300px;
    width: 800px;
  }
}
@media only screen and (max-width: 1000px) {
  .parent-col {
    display: flex;
    flex-direction: column;
  }

  .left-col {
    position: relative;
    width: 100%;
    margin-bottom: 2rem;
  }

  .right-col {
    position: relative;
    margin-left: 0;
    width: 100%;
  }
}
</style>
