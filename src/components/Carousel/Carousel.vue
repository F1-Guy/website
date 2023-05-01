<script lang="ts">
import { PropType } from "vue";
import Card from "./Card.vue";

export type CardType = {
    title: string,
    imageName: string
}

export default {
    components: {
        Card
    },

    props: {
        cards: {
            type: Object as PropType<CardType[]>,
            required: true
        }
    },

    methods: {

    }

}
</script>

<template>
    <div class="container">
        <h1 class="fw-bold text-center text-white">Skill issue</h1>
        <div class="d-flex flex-row">
            <div class="d-none d-md-flex align-items-center text-center"><i class="bi bi-caret-left-fill"></i></div>

            <div id="skills" class="position-relative overflow-hidden flex-grow-1" style="height: 500px;">
                <Card v-for="card in cards" :title="card.title" :image-name="card.imageName" class="card-center" />
            </div>

            <div class="d-none d-md-flex align-items-center text-center"><i class="bi bi-caret-right-fill"></i></div>
        </div>
    </div>
</template>

<style scoped>
.card-center {
    margin: auto;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
}

.bi {
    font-size: 3rem;
    color: white;
}
</style>

