<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data() {
        return {
            name: "Bartol Čagalj",
            ipa: "bar̩tol t͡ʃǎɡaʎ",
            isMouseOver: false
        }
    },
})
</script>

<template>
    <div id="about" class="row container">
        <div class="col py-3 phone-align-center">
            <h1 class="text-light fw-bold huge">I'm Čagalj,</h1>
            <h1 @mouseover="isMouseOver = true"
                @mouseleave="isMouseOver = false"
                class="text-light fw-bold huge"
                :class="{ 'ipa-font': isMouseOver }">
                {{ isMouseOver ? ipa : name }}
            </h1>
        </div>
        <div class="col profile phone-hide">
            <img src="../assets/images/temp.png" class="img-fluid" alt="Responsive image">
        </div>
    </div>

    <div class="container py-3">
        <p class="text-light text-center">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Mollitia deserunt qui quos atque ipsa illo adipisci,
            aspernatur quaerat tempore, nihil perspiciatis quas quidem, ab labore. Atque nam doloremque repellendus dolorum! Lorem ipsum, dolor
            sit amet consectetur adipisicing elit. Mollitia deserunt qui quos atque ipsa illo adipisci,aspernatur quaerat tempore, nihil
            perspiciatis quas quidem, ab labore. Atque nam doloremque repellendus dolorum!
        </p>
    </div>
</template>

<style scoped>
.huge {
    font-size: 5em;
}

/* The default font does not support IPA characters properly */
.ipa-font {
    font-family: 'Times New Roman', Times, serif;
}

@media (max-width: 768px) {
    .phone-hide {
        display: none;
    }

    .phone-align-center {
        text-align: center;
    }
}
</style>
