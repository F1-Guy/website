<script setup lang="ts">
</script>

<template>
    <div id="projects" class="container py-3">
        <h1 class="pb-1 fw-bold text-center text-white">My projects</h1>
        <p class="text-center text-white">Here are some of my projects. I'm always working on something (not necessarily programming).</p>
        <div class="row row-cols-1 row-cols-md-3 g-4">
            <div class="col">
                <div id="card" class="card h-100">
                    <img src="https://mdbcdn.b-cdn.net/img/new/standard/city/044.webp" class="card-img-top" alt="Skyscrapers" />
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aperiam suscipit hic maxime non unde vero saepe placeat
                            iusto corrupti nisi alias optio mollitia maiores, iure libero nobis tempora aut aliquid.
                        </p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div id="card" class="card h-100">
                    <img src="https://mdbcdn.b-cdn.net/img/new/standard/city/043.webp" class="card-img-top" alt="Los Angeles Skyscrapers" />
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">
                        </p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div id="card" class="card h-100">
                    <img src="https://mdbcdn.b-cdn.net/img/new/standard/city/042.webp" class="card-img-top" alt="Palm Springs Road" />
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">
                            Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
    background-color: #464646;
    border: none;
    border-radius: 10px;
    color: #ffffff;
    transition: all 0.2s ease-in-out;
}

.card:hover {
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    transform: translateY(-5px);
}

.card-title {
    font-size: 1.2rem;
    font-weight: bold;
}

.card-img-top {
    border-radius: 10px 10px 0 0;
}
</style>
