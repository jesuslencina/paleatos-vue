<template>
    <main>
        <div class="bg-sushi-1"></div>
        <div class="bg-sushi-2"></div>
        <img class="logo" src="../assets/images/logo.webp" alt="Logo de PALEATOS" draggable="false" width="50" height="60" />
        <h1>En el mundo se talan 20 millones de árboles anuales.</h1>
        <div class="line"></div>
        <p>
            Todo esto para hacer palitos de sushi desechables y así, satisfacer la actual demanda. En Chile, un local puede llegar usar hasta 20.000 palitos
            mensuales, (equivalente a 5 árboles talados).
        </p>
        <div class="caret">
            <span>Scrolleá</span>
            <img width="50" height="50" class="caret-icon" src="../assets/images/caret-down.webp" alt="Icono de flecha hacia abajo" />
        </div>
    </main>
</template>

<style scoped lang="scss">
    main {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 100vh;
        position: relative;
        overflow-x: hidden;
    }

    .logo {
        margin-top: 5vh;
        margin-bottom: 15vh;

        animation: swing-bottom-fwd 1.25s ease-in-out 5s both;
    }

    h1 {
        color: $accent-green;
        font-weight: 400;
        font-size: 2rem;
        line-height: 2.75rem;
        text-align: center;
        margin: 0 $spacing;

        animation: scale-up-center-fade 1.25s ease-in-out 1s both;
    }

    .line {
        margin-top: 3vh;
        width: 80vw;
        height: 1rem;
        @include bg-graphic("../assets/images/green-line.webp");

        animation: scale-up-center-fade 1.25s ease-in-out 2s both;
    }

    p {
        text-align: center;
        margin: 4vh $spacing 0;

        animation: scale-up-center-fade 1.25s ease-in-out 2.5s both;
    }

    .bg-sushi-1 {
        z-index: -1;
        position: absolute;
        left: 0;
        top: -30vh;
        width: 30vw;
        height: 100%;
        @include bg-graphic("../assets/images/hero-left.webp");
        @include shadow();

        animation: slide-right 1.25s ease-in-out 4s both;
    }

    .bg-sushi-2 {
        z-index: -1;
        position: absolute;
        right: 0;
        top: -40vh;
        width: 30vw;
        height: 100%;
        @include bg-graphic("../assets/images/hero-right.webp");
        @include shadow();

        animation: slide-left 1.25s ease-in-out 4s both;
    }

    .caret {
        display: flex;
        flex-direction: column;
        align-items: center;
        color: $accent-green;
        font-size: 0.9rem;
        margin-top: 5vh;
        animation: scale-up-center-fade 1.25s ease-in-out 5s both;

        &-icon {
            animation: levitate 1s alternate-reverse infinite;
        }
    }

    @media screen and (min-width: $desktop) and (orientation: landscape) {
        main {
            height: 100vh;
        }

        .logo {
            width: 6rem;
            height: auto;
            margin-bottom: 5vh;
        }

        h1 {
            font-size: 3rem;
            line-height: 4rem;
        }

        h1,
        p {
            margin-left: 25vw;
            margin-right: 25vw;
        }

        .bg-sushi-1 {
            z-index: unset;
            top: 0;
            left: -5vw;
        }

        .bg-sushi-2 {
            z-index: unset;
            top: -7.5vh;
            right: -5vw;
        }
    }
</style>
