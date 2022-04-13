<template>
<div class="container conttt" id="resume">
    <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="section-title text-center">
            <h2 class='fw-bold mb-5 p-5'>Resume</h2>
          </div>
        </div>
      </div>
   <div class="timeline-block timeline-block-right">
      <div class="marker"></div>
      <div class="timeline-content">
         <h3>January-December 2015</h3>
         <span>Bulumko High</span>
         <p>I Finished my matric in 2015 at Bulumko High</p>
      </div>
   </div>

   <div class="timeline-block timeline-block-left">
      <div class="marker"></div>
      <div class="timeline-content">
         <h3>January2016-December2018</h3>
         <span>College of Cape Town</span>
         <p>I did a 3 year IT course </p>
      </div>
   </div>

   <div class="timeline-block timeline-block-right">
      <div class="marker"></div>
      <div class="timeline-content">
         <h3>January2019-August2021</h3>
         <span>Salon Assistant</span>
         <p>I worked as an Assistant in my sister's salon i was doing appointment bookings for clients and i would also help with doing braids</p>
      </div>
   </div>

   <div class="timeline-block timeline-block-left">
      <div class="marker"></div>
      <div class="timeline-content">
         <h3>September 2021-March2022</h3>
         <span>Life Choices</span>
         <p>I recently finished my 6 months Full Stack development course at Life Choices</p>
      </div>
   </div>
</div>
  <div class="container">
    <hr>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.container {
   width: 80%;
   padding: 50px 0;
   margin: 50px auto;
   position: relative;
   overflow: hidden;
}

.container:before {
   position: absolute;
   top: 0;
   left: 50%;
   margin-left: -1px;
   width: 2px;
   height: 100%;
   background: #4d74b3;
   z-index: 1
}

.timeline-block {
   width: -webkit-calc(50% + 8px);
   width: -moz-calc(50% + 8px);
   width: calc(50% + 8px);
   display: -webkit-box;
   display: -webkit-flex;
   display: -moz-box;
   display: flex;
   -webkit-box-pack: justify;
   -webkit-justify-content: space-between;
   -moz-box-pack: justify;
   justify-content: space-between;
   clear: both;
}

.timeline-block-right {
   float: right;
}

.timeline-block-left {
   float: left;
   direction: rtl
}

.marker {
   width: 16px;
   height: 16px;
   border-radius: 50%;
   border: 2px solid #F5F7FA;
   background: #e23359;
   margin-top: 10px;
   z-index: 9999
}

.timeline-content {
   width: 95%;
   padding: 0 15px;
   color: #666
}

.timeline-content h3 {
   margin-top: 5px;
   margin-bottom: 5px;
   font-size: 25px;
   font-weight: 500;
   color: black;
}

.timeline-content span {
   font-size: 15px;
   color: #a4a4a4;
}

.timeline-content p {
   font-size: 14px;
   line-height: 1.5em;
   word-spacing: 1px;
   color: #888;
}


@media screen and (max-width: 768px) {
   .container:before {
      left: 8px;
      width: 2px;
   }
   .timeline-block {
      width: 100%;
      margin-bottom: 30px;
   }
   .timeline-block-right {
      float: none;
   }

   .timeline-block-left {
      float: none;
      direction: ltr;
   }
}

</style>