<script lang="ts">
export default {
    props: {
        title: String,
        imageName: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="`src/assets/logos/${imageName}`" class="emblem" />
        <h2 class="text-center text-white fw-bold py-3">{{ title }}</h2>
    </div>
</template>

<style scoped>
.card {
    background-color: transparent;
    border: 0;
    width: 20em;
    height: 20em;
}

.emblem {
    height: 100%;
    height: 100%;
}
</style>

