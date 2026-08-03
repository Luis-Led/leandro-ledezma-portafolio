<script setup>
import { ref, computed } from "vue";
import sisVenta from "./../images/localstorage.png";
import rickMorty from "./../images/rick-morty.png";
import pokedex from "./../images/pokeapi.png";
import dragonBall from "./../images/dragonball.png";
import lucifer from "./../images/lucifer.png";

const categoriaSelecionada = ref('All');
const categorias = ref(['All', 'APIs', 'HTML', 'Full-Stack']);

const proyectos = [
    {
        id: 1,
        nombre: "Rick & Morty",
        categoria: "APIs",
        framework:"React",
        image:rickMorty,
        link:"https://luis-led.github.io/rick-and-morty-react/"
    },
    {
        id: 2,
        nombre: "Pokedex",
        framework:"Vue",
        categoria: "APIs",
        image:pokedex,
        link:"https://luis-led.github.io/Poke_API/#/"
    },
    {
        id: 3,
        nombre: "Dragon Ball",
        categoria: "APIs",
        framework:"React",
        image:dragonBall,
        link:"https://luis-led.github.io/dragon-ball-react/"
    },
    {
        id: 4,
        nombre: "Landing Page",
        categoria: "HTML",
        framework:"CSS",
        link:"https://luis-led.github.io/Netflix/",
        image:lucifer
    },
    {
        id: 5,
        nombre: "Sistema de ventas Demo",
        categoria: "Full-Stack",
        framework:"JS,  HTML, CSS",
        image:sisVenta,
        link:"https://luis-led.github.io/H-compa-venta/login.html"

    },
];
const proyectosFiltrados = computed(() => {
    if (categoriaSelecionada.value === 'All') {
        return proyectos;
    }
    return proyectos.filter(
        proyecto => proyecto.categoria === categoriaSelecionada.value
    );
});
</script>

<template>
    <main>
        <section class="about-content px-5 py-5">
            <!-- <Menu/> -->
            <h1>Portafolio</h1>
            <div class="row">
                <div class="col-12">
                    <nav>
                        <ul class="list-unstyled d-flex gap-4 mt-2">
                            <!-- <li>
                                <a class=" text-decoration-none text-light "
                                    :class="categoriaSelecionada === 'APIs' ? 'activo' : 'normal'"
                                    @click="categoriaSelecionada = 'APIs'">APIs</a>
                            </li>
                            <li>
                                <a class="text-decoration-none text-light"
                                    :class="categoriaSelecionada === 'HTML' ? 'activo' : 'normal'"
                                    @click="categoriaSelecionada = 'HTML'">HTML</a>
                            </li>
                            <li>
                                <a class="text-decoration-none text-light"
                                    :class="categoriaSelecionada === 'Full-Stack' ? 'activo' : 'normal'"
                                    @click="categoriaSelecionada = 'Full-Stack'">Full-Stack</a>
                            </li> -->

                            <li v-for="categoria in categorias" :key="categoria">
                                <a class="text-decoration-none text-light"
                                    :class="{ activo: categoriaSelecionada === categoria }"
                                    @click="categoriaSelecionada = categoria">
                                    {{ categoria }}
                                </a>
                            </li>
                        </ul>
                    </nav>

                    <div class="row mt-4">
                        <div class="col-md-4 mb-3" v-for="proyecto in proyectosFiltrados" :key="proyecto.id">
                            <div class="card p-3">
                                <h4>{{ proyecto.nombre }}</h4>
                                <p>{{ proyecto.categoria }} - {{ proyecto.framework }}</p>
                                <a :href="proyecto.link" target="_blank" rel="noopener noreferrer"><img :src="proyecto.image" alt="" class="img-fluid"></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style scoped>
main {
    background-color: #111111;
    border-radius: 20px;
    color: white;
    position: relative;
}

.normal {
    background: transparent;
    /* color: white; */
    border-radius: 0px;

}

.activo {

    color: #FFC107 !important;
    border-bottom: 1px solid #FFC107;
    border-radius: 0px;
}

.card {
    background: #222;
    color: white;
    border-radius: 10px;
}

nav ul li a {
    cursor: pointer;
}

nav ul li a:not(.activo):hover {
    color: rgb(158, 158, 158) !important;
}
</style>