<template>
 <div class="services py-5" id="testimonials">
    <div class="container py-4">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="section-title text-center">
            <h2 class='fw-bold mb-5'>Testimonials</h2>
          </div>
        </div>
      </div>
      <div class="row text-center" v-if="testimonials">
        <div class="col-md-6 col-lg-4 mb-4" v-for="testimonial of testimonials"
          :key="testimonial.id">
     <img :src="testimonial.img" class="rounded-circle"> 
    
          
            <h3>{{ testimonial.fname }} {{ testimonial.lname }}</h3>
            <h3 class='fs-5 py-2'>{{ testimonial.status }}</h3>
            <p class='text-muted'>{{ testimonial.text }}</p>
          </div>
        </div>
      </div>
    </div>
  <div class="container">
    <hr>
  </div>
</template>

<script>
import App from "../App.vue";
export default {
  components:{
  },
  data() {
    return {
      testimonials: null,
    };
  },
  mounted() {
    fetch("https://portfolio-project-testimonial.herokuapp.com/testimonials")
      .then((response) => response.json())
      .then((data) => (this.testimonials = data))
      .catch((err) => console.log(err.message));
  },
  name: "testimonials",
  components: {
    App,
  },
};
</script>


<style scoped>
.col {
    margin-top: 0;
    margin-bottom: 60px;
    text-align: center;
}
img{
  width: 80px;
  height: 80px;
  object-fit: cover;
}
</style>