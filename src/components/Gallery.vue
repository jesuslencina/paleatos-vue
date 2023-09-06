<script>
    import Line from "./misc/Line.vue";

    export default {
        components: { Line },
    };
</script>

<template>
    <section>
        <div class="text">
            <h2>Galería</h2>
            <Line />
        </div>

        <div class="gallery">
            <img src="../assets/images/grid1.webp" alt="Foto de Paleatos sobre una mesa" />
            <img src="../assets/images/grid2.webp" alt="Foto de Paleatos sosteniendo una pieza de sushi" />
            <img
                src="../assets/images/grid3.webp"
                alt="Foto de una mesa llena de piezas de sushi, con diferentes partes de paleato agarrándolos para comerlos" />
            <img src="../assets/images/grid4.webp" alt="Persona haciendo una cara graciosa poniéndose Paleatros como bigote y piezas de sushi como ojos" />
        </div>
    </section>
</template>

<style scoped lang="scss">
    section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        overflow-x: hidden;
    }

    .text {
        margin-left: $spacing;
        margin-right: $spacing;
        text-align: center;
        margin-top: 5vh;
        margin-bottom: 4vh;

        h2 {
            color: $accent-green;
        }
    }

    .gallery {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        gap: 0.5rem;
        margin-left: 0.5rem;
        margin-right: 0.5rem;
        grid-template-areas:
            "first second fourth"
            "first third fourth";

        img {
            width: 100%;
            height: 100%;

            &:nth-child(1) {
                grid-area: first;
            }
            &:nth-child(2) {
                grid-area: second;
            }
            &:nth-child(3) {
                grid-area: third;
            }
            &:nth-child(4) {
                grid-area: fourth;
            }
        }
    }

    @media screen and (min-width: $desktop) and (orientation: landscape) {
        .text {
            margin-left: calc($spacing * 2);
            margin-right: calc($spacing * 2);
        }

        .gallery {
            gap: 1.25rem;
            margin-left: 1.25rem;
            margin-right: 1.25rem;
        }
    }
</style>
