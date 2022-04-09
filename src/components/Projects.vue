<template> 
<div class="services py-5" id="projects">
    <div class="container-lg py-4">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="section-title text-center">
            <h2 class='fw-bold mb-5'>Projects</h2>
          </div>
        </div>
      </div>

  <div class="row row-cols-1 row-cols-md-3 g-4">
  <div class="col" v-if="projects">
    <div class="card" v-for="project of projects" :key="project.id">
      <img :src="project.img_url" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{ project.title }}</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  </div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  </div>
  </div>
</template>

<script>
import App from "../App";
export default {
  data() {
    return {
      projects: [],
    };
  },

  mounted() {
    fetch("https://portfolio-project-testimonial.herokuapp.com/projects")
      .then((res) => res.json())
      .then((data) => (this.projects = data))
      .catch((err) => console.log(err.message));
  },
  name: "project",
  components: {
    App,
  },
};
</script>

<style scoped>

</style>