<script>
    import Line from "./misc/Line.vue";

    export default {
        components: { Line },
    };
</script>

<template>
    <section>
        <img src="../assets/images/about-mesita.webp" alt="Mesa de tronco con sushi" />
        <div class="text">
            <h2>Quiénes somos</h2>
            <Line />
            <p>
                Buscamos crear las mejores alternativas comestibles a palitos de sushi o cualquier otro elemento desechable involucrado en la comida. ¡Así
                podemos unirnos al movimiento de cuidar el planeta y juntxs reducir nuestros desechos!
            </p>
        </div>
    </section>
</template>

<style scoped lang="scss">
    section {
        animation: scale-up-center-fade 1.25s ease-in-out 5s both;
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
        margin-bottom: 10vh;
    }

    h2 {
        color: $accent-green;
    }

    @media screen and (min-width: $desktop) and (orientation: landscape) {
        .text {
            margin-left: calc($spacing * 2);
            margin-right: calc($spacing * 2);
        }
    }
</style>
