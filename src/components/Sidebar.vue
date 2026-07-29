<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const mostrar = ref(true);

const actualizarVista = () => {
  if (window.innerWidth <= 768|| window.innerWidth <= 992) {
    mostrar.value = false;
  } else {
    mostrar.value = true;
  }
};

onMounted(() => {
  actualizarVista(); // Estado inicial
  window.addEventListener("resize", actualizarVista);
});

onUnmounted(() => {
  window.removeEventListener("resize", actualizarVista);
});
</script>

<template>
  <aside class="d-flex flex-column align-items-center">
    <div class="menu text-center">  
      <img src="./../images/1735842047049.jpeg" class="avatar w-50 rounded-circle mb-3 mt-3" alt="Mi foto">
      <div class="menu-body">
        <h5 class="fw-bold text-light">Leandro Ledezma</h5>
        <span class="badge bg-secondary text-dark">Full Stack Web Developer</span>
      </div>  
    </div>
    <hr class="w-75">

    <button class="btn text-warning btn-toggle border-0 flecha" @click="mostrar = !mostrar">
      <i :class="mostrar ? 'bi bi-chevron-up' : 'bi bi-chevron-down'"></i>
    </button>

    <Transition name="desplegar">
      <ul class="list-unstyled" v-if="mostrar">

        <li class="d-flex align-items-center">
          <i class="bi bi-envelope text-warning m-4 fs-3"></i>
          <div >
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
              class="text-decoration-none text-light">linkedin.com/in/leandro-ledezma/</a>
          </div>
        </li>
      </ul>
    </Transition>
  </aside>

</template>

<style scoped>
aside {
  background-color: #111111;
  border-radius: 20px;
  position: sticky;
  top: 20px;
  /* Distancia desde la parte superior */
  align-self: start;
}

aside ul li {
  max-width: 300px;
  color: white;
}

.btn-toggle {
  display: none;
}

@media (max-width:768px){

    aside{
        position: relative;
        top: 0;
    }

    .btn-toggle{
        display: block;
        position: absolute;
        top: 1px !important ;
        right: 1px !important;
        background: #1b1b1b;
        border: 1px solid #444;
        width: 40px;
        height: 40px;
        z-index: 10;
        border-radius: 20px;
        
    }
    aside .avatar{
        width: 100px !important;
    }
    aside .menu{
      display: flex;
      align-items: center;
      gap: 10px;
    }

}

@media (max-width:992px){

    aside{
        position: relative;
        top: 0;
    }

    .btn-toggle{
        display: block;
        position: absolute;
        top: 15px;
        right: 15px;
        background: #1b1b1b;
        border: 1px solid #444;
        width: 40px;
        height: 40px;
        z-index: 10;
        
    }
}



.desplegar-enter-active,
.desplegar-leave-active {
  transition: opacity .5s ease, transform .5s ease;
}

.desplegar-enter-from,
.desplegar-leave-to {
  opacity: 0;
  transform: translateY(-15px);
}

.desplegar-enter-to,
.desplegar-leave-from {
  opacity: 1;
  transform: translateY(0);
}
</style>
