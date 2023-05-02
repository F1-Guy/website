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

    data() {
        return {
            currentIndex: 0
        }
    },

    methods: {
        getClass(index: number) {
            if (index === this.currentIndex) {
                return "active";
            } else if (index === this.currentIndex - 1) {
                return "left-from-active";
            } else if (index === this.currentIndex + 1) {
                return "right-from-active";
            } else {
                return "inactive";
            }
        },

        scrollLeft() {
            this.currentIndex--;

            if (this.currentIndex < 0) {
                this.currentIndex = this.cards.length - 1;
            }

            console.log(this.currentIndex);
        },

        scrollRight() {
            this.currentIndex++;

            if (this.currentIndex >= this.cards.length) {
                this.currentIndex = 0;
            }

            console.log(this.currentIndex);
        }
    }

}
</script>

<template>
    <div class="container">
        <h1 class="fw-bold text-center text-white">Skill issue</h1>
        <div class="d-flex flex-row">
            <div class="d-none d-md-flex align-items-center text-center"><i @click="scrollLeft" class="bi bi-caret-left-fill"></i></div>

            <div id="skills" class="position-relative overflow-hidden flex-grow-1" style="height: 500px;">
                <Card v-for="(card, index) in cards"
                      :key="index"
                      :class="getClass(index)"
                      :title="card.title"
                      :image-name="card.imageName"
                      class="card-center disable-select" />
            </div>

            <div class="d-none d-md-flex align-items-center text-center"><i @click="scrollRight" class="bi bi-caret-right-fill"></i></div>
        </div>
    </div>
</template>

<style scoped>
.bi {
    font-size: 3rem;
    color: white;
}

.card-center {
    margin: auto;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
}

.disable-select {
    user-select: none;
    pointer-events: none;
}

.active {
    transform: scale(1.1);
}

.left-from-active {
    filter: brightness(0.7);
    transform: translateX(-150%) scale(0.6);
}

.right-from-active {
    filter: brightness(0.7);
    transform: translateX(150%) scale(0.6);
}

.inactive {
    /* !important to override display: flex */
    display: none !important;
}
</style>

