<template>
  <aside class="d-flex flex-column align-items-center">
    <img src="./../images/1735842047049.jpeg" class="avatar w-50 rounded-circle mb-3 mt-3" alt="Mi foto">
    <h5 class="fw-bold text-light">Leandro Ledezma</h5>
    <span class="badge bg-secondary text-dark">Full Stack Web Developer</span>
    <hr class="w-75">
    <ul class="list-unstyled ">

      <li class="d-flex align-items-center">
        <i class="bi bi-envelope text-warning m-4 fs-3"></i>
        <div>
          <span class="d-block text-secondary small">Contact</span>
          <a href=" mailto: lleandroledezma@gmail.com" target="new_blank"
            class="text-decoration-none text-light">lleandroledezma@gmail.com</a><!--agrega tu correo -->
          <span class="fw-light"></span>
        </div>
      </li>

      <li class="d-flex align-items-center">
        <i class="bi bi-phone text-warning m-4 fs-3"></i>
        <div>
          <span class="d-block text-secondary small">Phone</span>
          <a href=" https://wa.me/59161814110" target="new_blank" class="text-decoration-none text-light">+591
            61814110</a><!-- Agrega tu número de teléfono a whatsapp -->
        </div>
      </li>

      <li class="d-flex wrap align-items-center">
        <i class="bi bi-geo-alt text-warning m-4 fs-3"></i>
        <div>
          <span class="d-block text-secondary small">Location</span>
          <span class="fw-light">Cochabamba - Bolivia</span>
        </div>
      </li>

      <li class="d-flex wrap align-items-center">
        <i class="bi bi-linkedin text-warning m-4 fs-3"></i>
        <div>
          <span class="d-block text-secondary small">Linkedin</span>
          <a href="https://www.linkedin.com/in/leandro-ledezma/" target="new_blank"
            class="text-decoration-none text-light">www.linkedin.com/in/leandro-ledezma/</a>
        </div>
      </li>
    </ul>
  </aside>

</template>
<style scoped>

aside{
    background-color: #111111;
    border-radius: 20px;
    position: sticky;
    top: 20px; /* Distancia desde la parte superior */
    align-self: start;
}
aside ul li{
    max-width: 300px;
    color: white;
}

</style>
