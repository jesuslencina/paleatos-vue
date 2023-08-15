<script>
import Line from "./misc/Line.vue";

export default {
    components: { Line },
};
</script>

<template>
    <section>
        <div class="text">
            <h2>Nuestro equipo</h2>
            <Line />
        </div>
    </section>
</template>

<style scoped lang="scss">
section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

img {
    width: 100%;
}

.text {
    margin-left: $spacing;
    margin-right: $spacing;
    text-align: center;
    margin-top: 5vh;
    margin-bottom: 40vh;
}

h2 {
    color: $accent-green;
}

@media screen and (min-width: $desktop) {
    .text {
        margin-left: calc($spacing * 2);
        margin-right: calc($spacing * 2);
    }
}
</style>
