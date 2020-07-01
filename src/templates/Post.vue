<template>
  <Layout>
    <div class="project-info">
      <div class="project-name project-child">
        <p class="cap_small">Project Name</p>
        <p id="title">{{$page.post.title}}</p>
      </div>
      <div class="project-description project-child">
        <p class="cap_small">Project Description</p>
        <p>{{$page.post.Description50}}</p>
        <p id="collab">{{$page.post.Collaborator}}</p>
      </div>
      <div class="project-year project-child">
        <p class="cap_small">Year</p>
        <p>{{$page.post.year}}</p>
        <p></p>
      </div>
      <div class="project-tags project-child">
        <p class="cap_small">Tags</p>
        <ul>
          <li v-for="tag in $page.post.Tags" :key="tag.id">{{tag}}</li>
        </ul>
      </div>
      <div class="project-links project-child">
        <p class="cap_small">Links</p>
        <ul v-for="link in $page.post.Links" :key="link.id">
          <li>
            <a v-bind:href="link.git[1]" target="_blank">{{link.git[0]}}</a>
          </li>
          <li>
            <a v-bind:href="link.project[1]" target="_blank">{{link.project[0]}}</a>
          </li>
          <li>
            <a v-bind:href="link.other[1]" target="_blank">{{link.other[0]}}</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="project-content">
      <div v-html="$page.post.content"></div>
    </div>
    <scrollTop />
  </Layout>
</template>


<page-query>
query ($path: String!) {
  post(path: $path) {
  	title
    Description50
    year
    Tags
    Links{
      git
      project
      other
    }
    Collaborator
    content
  }
}
</page-query>

<script scoped>
import scrollTop from "../components/scrollTop";

export default {
  components: { scrollTop }
};
</script>

<style>
b {
  font-weight: 400;
}
.caption {
  font-size: 12px;
  color: grey;
}

.project-info a,
.project-content a {
  text-decoration: none;
  color: var(--global-font-color);
}

.project-info a:hover,
.project-content a:hover {
  color: var(--highlight-blue);
}

.project-info {
  display: grid;
  grid-template-columns: 200px 5fr 1.5fr 2fr 200px;
  column-gap: 10px;
}

.project-info p {
  margin: 0;
}

.project-info ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

.project-content {
  margin-left: 210px;
  margin-right: 210px;
  margin-top: 50px;
}

.project-content img {
  box-sizing: border-box;
  width: 100%;
}

.project-year {
  padding-left: 40px;
}

.project-name #title {
  font-weight: 400;
  font-family: "Rozha One", serif;
  font-size: 25px;
}

#collab {
  font-size: 15px;
  margin-top: 3px;
  font-weight: 400;
}
@media only screen and (max-width: 1000px) {
  .project-info div {
    padding-bottom: 20px;
  }

  .project-content {
    box-sizing: border-box;
    margin-left: 0px;
    margin-right: 0px;
    margin-top: 40px;
  }

  .project-info {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .project-year,
  .project-name,
  .project-links,
  .project-tags {
    order: 1;
  }

  .project-description {
    order: 2;
  }
}

@media only screen and (max-width: 600px) {
  .project-info div {
    padding-bottom: 20px;
  }

  .project-name,
  .project-year {
    order: 1;
  }

  .project-description {
    order: 3;
  }

  .project-links,
  .project-tags {
    order: 3;
  }

  .project-year {
    padding-left: 0px;
  }
}
</style>