<template>
  <section class="contact py-5" id="contact">
  <div class="container-lg py-4">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="section-title text-center">
          <h2 class='fw-bold mb-5'>Contact Me</h2>
        </div>
      </div>
    </div> 
    <div class="row">
      <div class="col-md-5">
        <div class="contact-item d-flex">
          <div class="icon fs-4 text-danger">
            <i class="fas fa-envelope"></i>
          </div>
          <div class="text ms-3">
            <h3 class='fs-5'>Email</h3>
            <p classs='text-muted m-0'>zanelemoni4@gmail.com</p>
          </div>
        </div>
        <div class="contact-item d-flex mb-3">
          <div class="icon fs-4 text-danger">
            <i class="fas fa-phone"></i>
          </div>
          <div class="text ms-3">
            <h3 class='fs-5'>Phone</h3>
            <p classs='text-muted m-0'>062 433 4358</p>
          </div>
        </div>
        <div class="contact-item d-flex mb-3">
          <div class="icon fs-4 text-danger">
            <i class="fas fa-location-arrow"></i>
          </div>
          <div class="text ms-3">
            <h3 class='fs-5'>Address</h3>
            <p classs='text-muted m-0'>South Africa,Cape Town</p>
          </div>
        </div>                           
      </div>
      <div class="col-md-7">
        <div class="contact-form">
          <form @submit.prevent="handleSubmit"
              action="forms/contact.php"
              method="post"
              role="form"
              class="php-email-form">
            <div class="row">
              <div class="col-lg-6 mb-4">
                <input type="text" placeholder="Your Name" class='form-control form-control-lg fs-6 border-0 shadow-sm'
                    name="name"
                    v-model="name"
                    id="name"
                    required
                >

              </div>
              <div class="col-lg-6 mb-4">
                <input type="text" placeholder="Your Email" class='form-control form-control-lg fs-6 border-0 shadow-sm'
                 name="email"
                    v-model="email"
                    id="email"
                    required
                >                
              </div>              
            </div>
            <div class="row">
              <div class="col-lg-12 mb-4">
                <input type="text" placeholder="Subject" class='form-control form-control-lg fs-6 border-0 shadow-sm'>                
              </div>
            </div>
            <div class="row">
              <div class="col-lg-12 mb-4">
                <textarea rows='5' placeholder="Your message" class='form-control form-control-lg fs-6 border-0 shadow-sm'></textarea>                
              </div>
              
            </div> 
            
            <div class="row">
              <div class="col-lg-12">
                <button type='submit' class='btn btn-danger px-3'>Send Message</button>
              </div>
            </div>            
          </form>
        </div>
      </div>
    </div> 
  </div>
</section>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      subject: "",
      message: "",
    };
  },
    methods: {
      handleSubmit() {
  fetch('https://my-blogyy.herokuapp.com/contacts', {
    method: 'POST',
    body: JSON.stringify({
      name: this.name,
      email: this.email,
      subject: this.subject,
      message: this.message,
    }),
    headers: {
      'Content-type': 'application/json; charset=UTF-8',
    },
  })
    .then((response) => response.json())
    .then((data) =>(this.contact = data));
    alert("Message successfully sent").catch((err)=> console.log(err.message));
      },
    },
};
</script>

<style>

</style>