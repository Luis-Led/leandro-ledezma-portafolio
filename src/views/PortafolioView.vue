<script setup>
import { ref, computed } from "vue";
const categoriaSelecionada = ref('All');
const categorias = ref(['All', 'APIs', 'HTML', 'Full-Stack']);

const proyectos = [
    {
        id: 1,
        nombre: "Rick & Morty",
        categoria: "APIs",
    },
    {
        id: 2,
        nombre: "Pokedex",
        categoria: "APIs",
    },
    {
        id: 3,
        nombre: "Landing Page",
        categoria: "HTML",
    },
    {
        id: 4,
        nombre: "Sistema de ventas",
        categoria: "Full-Stack",
    },
];
const proyectosFiltrados = computed(() => {
        if(categoriaSelecionada.value === 'All') {
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
                                <a class="text-decoration-none text-light" :class="{ activo: categoriaSelecionada===categoria}" @click="categoriaSelecionada = categoria">
                                    {{ categoria }}
                                </a>
                            </li>
                        </ul>
                    </nav>

                    <div class="row mt-4">
                        <div class="col-md-4 mb-3" v-for="proyecto in proyectosFiltrados" :key="proyecto.id">
                            <div class="card p-3">
                                <h4>{{ proyecto.nombre }}</h4>
                                <p>{{ proyecto.categoria }}</p>
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