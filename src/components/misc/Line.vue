<template>
    <div class="line"></div>
</template>

<style scoped lang="scss">
    .line {
        @include bg-graphic("../../assets/images/line.webp");
        margin: 0 auto;
        width: 50vw;
        height: 2vh;

        @media screen and (min-width: $desktop) and (orientation: landscape) {
            width: 15vw;
        }
    }
</style>
