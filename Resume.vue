<template>
  <!------ Include the above in your HEAD tag ---------->

  <section class="experience pt-100 pb-100" id="experience">
    <div class="container">
      <div class="row">
        <div class="col-xl-8 mx-auto text-center"></div>
      </div>
      <div class="row">
        <div class="col-xl-12">
          <ul class="timeline-list">
            <!-- Single Experience -->
            <li>
              <div class="timeline_content">
                <span>2008</span>
                <h4>Intern Developer span</h4>
                <p>
                  We gather your business and products information. We then
                  determine the direction of the project and understand your
                  goals and we combine your ideas with ours for an amazing
                  website.
                </p>
              </div>
            </li>
            <!-- Single Experience -->
            <li>
              <div class="timeline_content">
                <span>2007-2012</span>
                <h4>Junior Developer</h4>
                <p>
                  We gather your business and products information. We then
                  determine the direction of the project and understand your
                  goals and we combine your ideas with ours for an amazing
                  website.
                </p>
              </div>
            </li>
            <!-- Single Experience -->
            <li>
              <div class="timeline_content">
                <span>2012-2015</span>
                <h4>Senior Developer</h4>
                <p>
                  We gather your business and products information. We then
                  determine the direction of the project and understand your
                  goals and we combine your ideas with ours for an amazing
                  website.
                </p>
              </div>
            </li>
            <!-- Single Experience -->
            <li>
              <div class="timeline_content">
                <span>2015-2018</span>
                <h4>Project Manager</h4>
                <p>
                  We gather your business and products information. We then
                  determine the direction of the project and understand your
                  goals and we combine your ideas with ours for an amazing
                  website.
                </p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.pt-100 {
  padding-top: 100px;
}
.pb-100 {
  padding-bottom: 100px;
}

ul.timeline-list {
  position: relative;
  margin: 0;
  padding: 0;
}
ul.timeline-list:before {
  position: absolute;
  content: "";
  width: 2px;
  height: 100%;
  background-color: #ff3636;
  left: 50%;
  top: 0;
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
}
ul.timeline-list li {
  position: relative;
  clear: both;
  display: table;
}
.timeline_content {
  border: 2px solid #ff3636;
  background-color: #fff;
}
ul.timeline-list li .timeline_content {
  width: 45%;
  color: #333;
  padding: 30px;
  float: left;
  text-align: right;
}
ul.timeline-list li:nth-child(2n) .timeline_content {
  float: right;
  text-align: left;
}
.timeline_content h4 {
  font-size: 22px;
  font-weight: 600;
  margin: 10px 0;
}
ul.timeline-list li:before {
  position: absolute;
  content: "";
  width: 25px;
  height: 25px;
  background-color: #ff3636;
  left: 50%;
  top: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  border-radius: 50%;
}
.timeline_content span {
  font-size: 18px;
  font-weight: 500;
  font-family: poppins;
  color: #ff3636;
}
</style>
