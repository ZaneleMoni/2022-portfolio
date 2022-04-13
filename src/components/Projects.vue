<template> 
    <section id="projects" class="projects py-5">
    <div class="container hr">
      <hr class="bg-white" />
    </div>
    <div class="container">
      <div class="pb-5 justify-content-center">
        <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="section-title text-center">
            <h2 class='fw-bold mb-5 p-5'>Projects</h2>
          </div>
        </div>
      </div>
        <div class="row col-lg-12 proji" style="row-gap: 30px">
          <div
            v-for="project of projects"
            :key="project.id"
            class="col-lg-3  col-md-6"
            style="display: flex; justify-content: center"
          >

            <div class="card ani-card card-shadow" style="width: 18rem">
              <img :src="project.img_url" class="card-img-top" alt="..." />
              <div class="card-body">
                <h4 class="card-title text-black">{{ project.title}}</h4>
                 <div class="links justify-content-center">
              <a :href="project.github" class="text-dark me-2" target="_blank"
                ><i class="fa fa-github"></i></a
              ><br />
              <a :href="project.netlify" class="text-dark me-2" target="_blank"
                ><i class="fa fa-netlify">
                  </i
              ></a>
            </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </section>
    <div class="container">
    <hr>
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
.card-shadow{
-webkit-box-shadow: -12px 11px 12px 2px rgba(118, 118, 118, 0.3); 
box-shadow:  -12px 11px 12px 2px rgba(75, 75, 75, 0.3);
      border: none;
}
    .card-img-top {
        height: 200px;
        width: 100%;
        object-fit: cover;

      }
</style>