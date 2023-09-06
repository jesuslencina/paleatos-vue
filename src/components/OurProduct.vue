<script>
    import Line from "./misc/Line.vue";

    export default {
        components: { Line },
    };
</script>

<template>
    <section>
        <div class="text">
            <h2>Nuestro producto</h2>
            <Line />
        </div>
        <p class="paragraph">
            Creemos que la simpleza es un camino que lleva a la felicidad, estamos convencidos que los detalles son los que marcan la diferencia, y nosotros
            queremos ser uno de ellos en tu comida. Queremos ser el cambio que haga que tu conversación en la mesa sea lo que pase a la historia y no la basura
            que dejas en ella”.
        </p>
        <div class="seal-container">
            <div class="seal">
                <img src="../assets/images/seal-1.webp" width="90" alt="Sello de calidad que dice '100% guarantee' (en inglés: garantía al 100%)" />
                <div>
                    <p>100% comestibles</p>
                    <p>100% veganos</p>
                </div>
            </div>
            <div class="seal">
                <img src="../assets/images/seal-2.webp" width="90" alt="Ilustración de dos manos dándose un apretón de manos como símbolo de compromiso" />
                <p>Valores nutricionales</p>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    section {
        margin-top: 7.5vh;
        margin-left: $spacing;
        margin-right: $spacing;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .text {
        text-align: center;
        margin-top: 5vh;

        h2 {
            color: $accent-green;
        }
    }

    .paragraph {
        text-align: center;
    }

    .seal-container {
        margin-top: 6vh;
        margin-bottom: 6vh;

        display: flex;
        flex-direction: column;
        gap: 4vh;

        .seal {
            display: grid;
            grid-template-columns: 1fr 2fr;
            align-items: center;
            justify-content: center;
            gap: 1rem;

            p {
                margin: 0;
                color: $accent-green;
                font-size: 1rem;
            }
        }
    }

    @media screen and (min-width: $desktop) and (orientation: landscape) {
        .paragraph {
            margin-left: calc($spacing * 1.25);
            margin-right: calc($spacing * 1.25);
        }

        .seal-container {
            flex-direction: row;
        }
    }
</style>
