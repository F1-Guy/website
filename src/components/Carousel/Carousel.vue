<script setup lang="ts">
import Card from "./Card.vue";
</script>

<template>
    <div class="container">
        <h1 class="fw-bold text-center text-white">Skill issue</h1>

        <!-- Fix this later for small screen size it does not center properly-->
        <div class="row d-flex justify-content-between align-items-center text-white">
            <span class="text-center arrow-controls "><i class="bi bi-caret-left-fill"></i></span>

            <Card title="C#" image-name="cs.svg" />

            <span class="text-center arrow-controls "><i class="bi bi-caret-right-fill"></i></span>
        </div>
    </div>
</template>

<style scoped>
.bi {
    font-size: 2em;
}

.arrow-controls {
    width: fit-content;
}

@media (max-width: 768px) {
    .arrow-controls {
        display: none;
    }
}
</style>

