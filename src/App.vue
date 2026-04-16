<script setup>
import { RouterLink, RouterView } from "vue-router";
import Sidebar from "./components/Sidebar.vue";
import Menu from "./components/Menu.vue";
import { useRouter } from "vue-router";
</script>

<template>
  
    <!-- <Menu /> -->
  <div class="container ">
  <!-- <div class="container-fluid py-5 d-flex justify-content-center gap-2"> -->
    <!-- <div class="row"> -->
      <!-- Sidebar -->
      <!-- <div class="col-12 col-md-3"> -->
        <Sidebar class="sidebar-area"/>
      <!-- </div> -->
      <!-- Contenido -->
      <!-- <div class="col-12 col-md-9"> -->
        <div class="main-area">
          <RouterView />
          <Menu class="menu-nav" />
        </div>
        
      <!-- </div> -->
    <!-- </div> -->
  </div>
</template>

<style scoped>
.container{
    
    min-height: 100vh;
    padding: 50px 20px ;
    flex: 1;
    display: grid;
    grid-template-areas:
    "aside main";
    grid-template-columns: 350px 1fr;
    grid-template-rows: 1fr;
    gap: 10px;
    align-items: start;
    position: relative;

}
.sidebar-area{
    grid-area: aside;
}
.main-area{
    grid-area: main;    
    position: relative;
}
/* @media (max-width: 992px) {
    .sidebar-area{
      position: relative;
      margin: 0 0 20px 0;
    }
    .container {
        grid-template-areas:
        "aside"
        "main";
        grid-template-columns: 1fr;
        grid-template-rows: 2fr;
        
        margin: 0 auto;
    }
} */
@media (max-width: 768px) {
    .container{
        grid-template-areas:
        "aside"
        "main";
        grid-template-columns: 1fr;
        grid-template-rows: 2fr;
        
        margin: 0 auto;
    }
    .sidebar-area{
      position: relative;
      margin: 0 0 20px 0;
    }
    
}


</style>
