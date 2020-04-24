<template>
  <Layout>
    <div class="project-info">
      <div class="project-name project-child">
        <p class="cap_small">Project Name</p>
        <p>{{$page.post.title}}</p>
      </div>
      <div class="project-description project-child">
        <p class="cap_small">Project Description</p>
        <p>{{$page.post.Description50}}</p>
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
        <ul>
          <li>
            <!-- <a href="$page.post.Project_Link">Project Link</a> -->
          </li>
          <li>Github Link</li>
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
    Git_link
    Project_Link
    Other_Link
    Collaborator
    content
  }
}
</page-query>

<script>
import scrollTop from "../components/scrollTop";

export default {
  components: { scrollTop }
};
</script>

<style>
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
  margin-top: 20px;
}

.project-content img {
  box-sizing: border-box;
  width: 100%;
}

.project-year {
  padding-left: 40px;
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
}
</style>