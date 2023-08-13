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
    </main>
</template>

<style scoped lang="scss">
$spacing: 8vw;

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
}

h1 {
    color: $accent-green;
    font-weight: 400;
    font-size: 2rem;
    line-height: 2.75rem;
    text-align: center;
    margin: 0 $spacing;
}

.line {
    margin-top: 3vh;
    width: 80vw;
    height: 1rem;
    @include bg-graphic("../assets/images/green-line.webp");
}

p {
    text-align: center;
    margin: 4vh $spacing 0;
}

.bg-sushi-1 {
    z-index: -1;
    position: absolute;
    left: 0;
    top: -30vh;
    width: 30vw;
    height: 100%;
    @include bg-graphic("../assets/images/hero-left.webp");
}

.bg-sushi-2 {
    z-index: -1;
    position: absolute;
    right: 0;
    top: -40vh;
    width: 30vw;
    height: 100%;
    @include bg-graphic("../assets/images/hero-right.webp");
}

@media screen and (min-width: $desktop) {
    .logo {
        width: 6rem;
        height: auto;
        margin-bottom: 15vh;
    }

    h1{
        font-size: 3rem;
        line-height: 4rem;
    }

    h1,
    p {
        margin-left: 25vw;
        margin-right: 25vw;
    }

    .bg-sushi-1 {
        top: 0;
        left: -5vw;
    }

    .bg-sushi-2 {
        top: -7.5vh;
        right: -5vw;
    }
}
</style>
