<script>
    import Line from "./misc/Line.vue";

    export default {
        components: { Line },
        data() {
            return {
                teamMembers: [
                    { picturePath: "img/members/member-1.webp", name: "Eytan Gottlieb", alias: "Sugo", role: "Confundador" },
                    { picturePath: "img/members/member-2.webp", name: "Mario Vergara", alias: "Malein", role: "Diseñador" },
                    { picturePath: "img/members/member-3.webp", name: "Tomas Hofman", alias: "Hof", role: "Confundador" },
                    { picturePath: "img/members/member-4.webp", name: "Pedro Iriberry", alias: "Peter, el sensei", role: "Asesor" },
                    { picturePath: "img/members/member-5.webp", name: "Diego Millan", alias: "Le practicien", role: "Ing. en Alimentos" },
                    { picturePath: "img/members/member-6.webp", name: "Tomás Pantoja", alias: "Tommy", role: "Ing. en Diseño" },
                ],
            };
        },
    };
</script>

<template>
    <section>
        <div class="text">
            <h2>Nuestro equipo</h2>
            <Line />
        </div>

        <div class="member-container">
            <article class="member" v-for="member of teamMembers">
                <img :src="member.picturePath" :alt="`${member.name}, ${member.role}`" />
                <div>
                    <strong class="name green">{{ member.name }}</strong>
                    <p class="green">{{ member.alias }}</p>
                    <strong>{{ member.role }}</strong>
                </div>
            </article>
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
        margin-bottom: 10vh;

        h2 {
            color: $accent-green;
        }
    }

    .member-container {
        display: flex;
        gap: 2rem;

        width: 100%;
        height: 45vh;
        overflow-x: scroll;

        .member {
            display: grid;
            grid-template-rows: 65% 1fr;
            justify-content: center;

            text-align: center;

            img {
                height: 100%;
            }

            strong.name {
                font-size: 1.5rem;
            }

            p {
                margin: 0 0.5rem;
            }

            .green {
                color: $accent-green;
            }

            &:first-child {
                padding-left: $spacing;
            }

            &:last-child {
                padding-right: $spacing;
            }
        }
    }

    @media screen and (min-width: $desktop) and (orientation: landscape) {
        .text {
            margin-left: calc($spacing * 2);
            margin-right: calc($spacing * 2);
        }

        .member-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            align-items: center;
            row-gap: 4rem;

            height: unset;
            overflow-x: unset;
            justify-content: center;

            .member {
                img {
                    width: 12rem;
                    object-fit: contain;
                }

                &:nth-child(5){
                    grid-column: 2;
                }

                &:first-child {
                    padding-left: unset;
                }

                &:last-child {
                    padding-right: unset;
                }
            }
        }
    }
</style>
