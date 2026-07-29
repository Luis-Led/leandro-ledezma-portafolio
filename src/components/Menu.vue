<template>
    <section class="d-flex justify-content-between main-content  ">
        <nav class="">
            <ul class="list-unstyled d-flex gap-5 pt-3 px-5">
                <li><RouterLink to="/">About</RouterLink></li>
                <li><RouterLink to="/resume">Resume</RouterLink></li>
                <li><RouterLink to="/portafolio" >Portafolio</RouterLink></li>
            </ul>
        </nav>


    </section>
</template>

<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<style scoped>
nav {
    background-color:#1f1f1f;
    border-radius: 0 20px 0 20px;
    /* padding: 10px; */
    position: absolute;
    top: 0;
    right: 0;
    border: 1px solid #555555;
    border-top: #000000;
    border-right: #000000;
}

a{
    color: white;
    text-decoration: none;
}

a:hover{
    color: #FFC107;
    text-decoration: underline;
    text-underline-offset: 10px;
}
.router-link-active {
    color: #FFC107;
    text-decoration: underline;
    text-underline-offset: 10px;
}
@media (max-width: 768px) {
    nav {
        
        border-radius: 20px 20px 0 0;
        /* position: static; */
        position: fixed;
        bottom: 0;
        width: 100%;
        top: auto;
        display: flex;
        justify-content: space-around;
    }
    ul {
        width: 100%;
        justify-content: space-around;
        padding: 10px;
        gap: 0;
    }
    .main-content {
    padding-bottom: 20px;
    }
}

@media (max-width: 992px) {
    nav {
        
        border-radius: 20px 20px 0 0;
        /* position: static; */
        position: fixed;
        bottom: 0;
        width: 100%;
        top: auto;
        display: flex;
        justify-content: space-around;
    }
    ul {
        width: 100%;
        justify-content: space-around;
        padding: 10px;
        gap: 0;
    }
    .main-content {
    padding-bottom: 20px;
    }
}

</style>