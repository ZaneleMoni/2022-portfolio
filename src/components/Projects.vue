<template>
    <section class="portfolio py-5" id='projects'>
    <div class="container-lg py-4">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="section-title text-center">
            <h2 class='fw-bold mb-5'>Works</h2>
          </div>
        </div>
      </div>    
      <div class="row">
        <div class="col-md-6 col-lg-4" v-if="projects">
          <div class="portfolio-item" v-for="project of projects" :key="project.id">
            <img :src="project.img_url" class='w-100 img-thumbnail' alt="portfolio-item">
            <h3 class='text-capitalize fs-5 my-2'>{{ project.title }}</h3>
            <p class='mb-5'><a href="#" class='text-danger text-decoration-none'>Live demo</a></p>
          </div>
        </div>
        <!-- <div class="col-md-6 col-lg-4">
          <div class="portfolio-item">
            <img src="https://i.postimg.cc/KvsrCG0q/2.jpg" class='w-100 img-thumbnail' alt="portfolio-item">
            <h3 class='text-capitalize fs-5 my-2'>app landing page</h3>
            <p class='mb-5'><a href="#" class='text-danger text-decoration-none'>Live demo</a></p>
          </div>
        </div> -->
        <!-- <div class="col-md-6 col-lg-4">
          <div class="portfolio-item">
            <img src="https://i.postimg.cc/yN0mJFst/3.jpg" class='w-100 img-thumbnail' alt="portfolio-item">
            <h3 class='text-capitalize fs-5 my-2'>creative team section</h3>
            <p class='mb-5'><a href="#" class='text-danger text-decoration-none'>Live demo</a></p>
          </div>
        </div> -->
        <!-- <div class="col-md-6 col-lg-4">
          <div class="portfolio-item">
            <img src="https://i.postimg.cc/TYPJkLJ5/4.jpg" class='w-100 img-thumbnail' alt="portfolio-item">
            <h3 class='text-capitalize fs-5 my-2'>toggle pricing table</h3>
            <p class='mb-5'><a href="#" class='text-danger text-decoration-none'>Live demo</a></p>
          </div>
        </div> -->
        <!-- <div class="col-md-6 col-lg-4">
          <div class="portfolio-item">
            <img src="https://i.postimg.cc/Nj38fNqR/5.jpg" class='w-100 img-thumbnail' alt="portfolio-item">
            <h3 class='text-capitalize fs-5 my-2'>bootstrap 5 image gallery</h3>
            <p class='mb-5'><a href="#" class='text-danger text-decoration-none'>Live demo</a></p>
          </div>
        </div>     -->
        <!-- <div class="col-md-6 col-lg-4">
          <div class="portfolio-item">
            <img src="https://i.postimg.cc/SsqWcJKs/6.jpg" class='w-100 img-thumbnail' alt="portfolio-item">
            <h3 class='text-capitalize fs-5 my-2'>filterable image gallery</h3>
            <p class='mb-5'><a href="#" class='text-danger text-decoration-none'>Live demo</a></p>
          </div>
        </div>                             -->
      </div>
    </div>
  </section>
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

<style>

</style>