<template>
  <section class="content text-white py-5 px-5">
        <h1 class="mb-4">Resume</h1>

        <ul class="list-unstyled mt-4 text-start timeline ">
          <li class="d-flex wrap align-items-center">
            <i class="bi bi-book text-warning m-4 fs-3"></i>
            <h3>Education</h3>
          </li>

          <li class=" timeline-item px-4 ">
            <span class="circle"></span>
            <div class="ms-5">  
              <h4>UAB - Universidad Adventista de Bolivia</h4>
              <p class="text-warning">2020 - 2024</p>
              <p>Bachelor's degree in System Engineer from Universidad Adventista de Bolivia.</p>
            </div>
          </li>

          <li class=" timeline-item px-4 ">
            <span class="circle"></span>
            <div class="ms-5">  
              <h4>Bootcamp Full Stack Developer – Hamilo</h4>
              <p class="text-warning">July - November - 2024</p>
              <p>I completed the Full Stack Developer Bootcamp at Hamilo, where I developed web applications with Vue, Node.js and Express, strengthening my frontend and backend skills.</p>
            </div>
          </li>
          <li class="timeline-item px-4 ">
            <span class="circle"></span>
            <div class="ms-5">  
              <h4>INTJEM - Instituto Tecnico Jesus Maria</h4>
              <p class="text-warning">2018 - 2020</p>
              <p>I graduated with a Higher Technician degree in Computer Systems..</p>
            </div>
          </li>
        </ul>

        <ul class="list-unstyled mt-4 text-start timeline">
          <li li class="d-flex wrap align-items-center">
            <i class="bi bi-person-workspace text-warning m-4 fs-3 "></i>
            <h3>Experience</h3>
          </li>

          <li class="timeline-item px-4 ">
            <span class="circle"></span>
            <div class="ms-5">  
              <h4>Full-Stack Developer - Talent Investment Platform (Bootcamp Project)</h4>
              <p class="text-warning">July 2024 - November 2024</p>
              <p>Built a web platform where investors funded talents, using Vue, Node.js, Express, and MySQL. Implemented authentication, roles, and investment features.</p>
            </div>
          </li>

          <li class="timeline-item px-4 ">
            <span class="circle"></span>
            <div class="ms-5">  
              <h4>December 2019 - February 2020</h4>
              <p class="text-warning">July 2024 - November 2024</p>
              <p> Assisted in preparing class materials, supporting students with development tools, and guiding them through package management and basic programming concepts.</p>
            </div>
          </li>
        </ul>

        

        <h2 class="mb-4 mt-5">My Skills</h2>

        <!-- Tarjetas responsivas -->
        <div class="row g-4">

            <div class="col-12">
              <div class="card bg-dark h-100 d-flex wrap p-1">
                <div class="card-body g-4">
                  <!-- <h5 class="card-title text-white">Web Development</h5> -->
                  <a class="btn btn-outline-light">HTML5 </a> <a class="btn btn-outline-light">CSS3</a> <a class="btn btn-outline-light">JavaScript</a> <a class="btn btn-outline-light">Vue</a> <a class="btn btn-outline-light">Node.js</a> <a  class="btn btn-outline-light">Express</a> <a class="btn btn-outline-light">MySQL</a> 
                </div>
              </div>
            </div>
          

          
        </div>
  </section>
</template>

<style scoped>
.content {
  /* background-color: var(--black-2); */
  background-color: #111111;
  border-radius: 20px;
  padding: 2rem;
}


.timeline {
  position: relative;
}

.timeline::before{
  content: "";
  position: absolute;
  top: 60px;
  left: 37px;
  width: 2px;
  height: calc(100% - 60px);
  background-color: #6c6c6c;
}

.timeline-item{
  position: relative;
  margin-top: 25px;
}

.timeline-item .circle{
  position: absolute;
  left: 30px;
  top: 5px;
  width: 14px;
  height: 14px;
  background: #ffc107;
  border-radius: 50%;
  border: 2px solid #6c6c6c;
}

.timeline-item:not(:last-child)::after{
  content: "";
  position: absolute;
  top: 60px;
  left: 37px;
  width: 2px;
  height: calc(100% - 60px);
  background-color: #6c6c6c;
}

</style>
