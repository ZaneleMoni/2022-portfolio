<template>
  <section class="home py-5" id="home">
    <div class="container-lg">
      <div class="row min-vh-100 align-items-center align-content-center">
        <div class="col-md-6 mt-5 mt-md-0">
          <div class="home-img text-center">
            <img
              src="https://i.postimg.cc/Kjt2QpKG/zanele2.jpg"
              class="rounded-circle mw-100 bg-danger"
              alt="profile-img"
            />
          </div>
        </div>
        <div class="col-md-6 mt-5 mt-md-0 order-md-first">
          <div class="home-text">
            <p class="text-muted mb-1">Hi there! I am a</p>
            <h1 class="text-danger text-uppercase fs-1 fw-bold">
              Full stack developer
            </h1>
            <h2 class="fs-4">Ntombizanele Moni</h2>
            <a
              href="https://codepen.io/ZaneleMoni"
              class="btn btn-danger px-3 mt-3"
              target="_blank"
              >My work</a
            >
          </div>
        </div>
      </div>
    </div>
  </section>
  <div class="container">
    <hr />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
img {
  height: auto;
  width: 550px;
  object-fit: cover;
}
</style>
