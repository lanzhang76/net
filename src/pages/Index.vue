<template>
  <div class="home">
    <Layout>
      <div class="main">
        <div class="container">
          <div v-for="edge in $static.allPost.edges" :key="edge.node.id">
            <div v-on:mouseover="changeURL(edge.node.cover_image,edge.node.Description10)">
              <g-link class="hover-title" :to="edge.node.path">
                <!-- <span>{{ hover ? '⧈' : '⧠' }}</span> -->
                ⧠
                <span
                  id="spantitle"
                  @mouseover="hover = true"
                  @mouseleave="hover = false"
                >{{edge.node.title}}</span>
              </g-link>
            </div>
            <!-- <g-image class="hover-image" :src="edge.node.cover_image"></g-image> -->
          </div>
        </div>
      </div>
      <!-- <Foofoo></Foofoo> -->
      <div class="header_element header2">
        <g-link class="nav__link" to="/about/">About</g-link>
      </div>
      <coverimage v-bind:url="currentURL" v-show="currentURL != ''" />
      <div id="shortDes">{{currentDescription}}</div>
    </Layout>
  </div>
</template>

<static-query>
{
 allPost(sortBy:"order"){
  edges{
    node{
      content
      title
      Description10
      Description50
      year
      path
      cover_image 
    }
  }
}
}
</static-query>

<script>
import Foofoo from "../components/Footer";
import coverimage from "../components/Cover";

export default {
  metaInfo: {
    title: "Work"
  },
  components: {
    Foofoo,
    coverimage
  },
  data() {
    return {
      currentURL: "",
      currentDescription: "A creative technlogist, developer and art director",
      hover: false
    };
  },
  methods: {
    changeURL: function(url, des) {
      this.currentURL = url.src;
      this.currentDescription = des;
    },
    fillcube: function() {
      console.log(this.$refs.cuberef.innerText);
      if (this.$refs.cuberef.innerText == "⧈") {
        this.$refs.cuberef.innerText = "⧠";
      } else {
        this.$refs.cuberef.innerText = "⧈";
      }
    }
  }
};
</script>

<style>
.main {
  left: 2rem;
  right: 2rem;
  padding-top: 1rem /*!main_margin*/;
  padding-bottom: 1rem /*!main_margin*/;
  padding-left: 1rem /*!main_margin*/;
  padding-right: 1rem /*!main_margin*/;
  margin: 0;
  position: absolute;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

.container {
  display: flex;
  flex-wrap: wrap;
  align-items: left;
  justify-content: left;
  padding: 10vh 0;
  font-family: "Rozha One", serif;
}

#shortDes {
  /* background-color: black;
  color: white; */
  font-family: "Poppins", sans-serif;
}

.header2 {
  position: fixed;
  right: 0px;
  bottom: 0;
  padding: var(--world-padding);
  font-size: var(--reg-font-size);
  z-index: 200;
}

.hover-title {
  margin: 10px;
  font-size: 50px;
  font-weight: 300;
  display: inline;
  pointer-events: auto;
  cursor: pointer;
  text-decoration: none;
  color: var(--global-font-color);
  margin-right: 20px;
}

.hover-title:hover {
}

#spantitle:hover {
  background-color: black;
  animation: fontchange 1s ease forwards;
}

@keyframes fontchange {
  0% {
    color: rgba(255, 173, 255, 1);
  }
  25% {
    color: rgba(173, 205, 255, 1);
  }
  50% {
    color: rgba(199, 255, 173, 1);
  }
  100% {
    color: rgba(255, 255, 255, 1);
  }
}

#shortDes {
  position: fixed;
  font-size: 20px;
}

@media only screen and (max-width: 600px) {
  #shortDes {
    display: none;
    background: coral;
  }

  .container {
    display: flex;
    flex-wrap: wrap;
    align-items: left;
    justify-content: left;
    padding: 10vh 0;
    font-size: 40px;
  }

  .main {
    left: 1rem;
    right: 1rem;
  }
}
</style>
