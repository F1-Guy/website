<script setup lang="ts">
</script>

<template>
    <!-- Debug overflow issue where position-absolute separates body form top of the page -->
    <section class="navigation container-fluid bg-dark">
        <nav id="nav" class="navbar navbar-expand-md navbar-dark">
            <a class="navbar-brand" href="#jumbo">Bartol Čagalj</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
                <span class="bi bi-three-dots"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-md-end" id="navbarNavDropdown">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#skills">Skills</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#projects">Projects</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">Contact</a>
                    </li>
                </ul>
            </div>
        </nav>
    </section>
</template>

<style scoped></style>
