<script setup>
import Menu from '../components/Menu.vue';

</script>
<template>
  
  <main>
            <section class="about-content px-5 py-5">
            <!-- <Menu/> -->
              <h1>About Me</h1>
                <div class="row">
                    <div class="col-12">
                        <p class="lead text-light mb-4">
                            I am <strong class="text-warning">Leandro Ledezma</strong>, <strong
                                class="text-warning">Systems Engineer</strong>
                            and <strong class="text-warning">Full Stack Developer</strong> passionate about creating
                            complete technological solutions
                            that solve real problems.
                        </p>

                        <p class="text-light mb-4">
                            With a solid background in <strong class="text-warning">Systems Engineering</strong>,
                            I master modern technologies
                            such as <strong class="text-warning">Vue.js, Node.js, Express and MySQL</strong> to build
                            robust and scalable web applications.
                            My comprehensive approach allows me to cover from backend architecture to intuitive user
                            experiences
                            on the frontend.
                        </p>

                        <p class="text-light mb-4">
                            Currently, I am in a process of <strong class="text-warning">continuous learning</strong>,
                            delving into
                            new technologies and staying updated with industry trends. As a
                            constantly evolving professional,
                            I apply best practices and modern design patterns in every project I develop.
                        </p>

                        <p class="text-light">
                            My goal is to transform ideas into <strong class="text-warning">attractive and functional
                                digital experiences</strong>,
                            providing value through clean, efficient and well-structured code. Let's connect and
                            make your digital vision a reality!
                        </p>

                        <!-- Tarjetas de estadísticas -->
                        <div class="row  g-4">
                            <div class="col-md-4">
                                <div class="stat-card text-center p-4">
                                    <i class="bi bi-code-slash fs-1 text-warning"></i>
                                    <h3 class="text-light mt-3">5+</h3>
                                    <p class="text-secondary">Proyectos Completados</p>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="stat-card text-center p-4">
                                    <i class="bi bi-database fs-1 text-warning"></i>
                                    <h3 class="text-light mt-3">MySQL</h3>
                                    <p class="text-secondary">Base de Datos Relacional</p>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="stat-card text-center p-4">
                                    <i class="bi bi-git fs-1 text-warning"></i>
                                    <h3 class="text-light mt-3">Github</h3>
                                    <p class="text-secondary">Control de Versiones</p>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </section>
        </main>
</template>

<style scoped>
main{
    background-color: #111111;
    border-radius: 20px;
    color: white;
    position: relative;
}
</style>
