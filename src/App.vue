<script>
    import Hero from "./components/Hero.vue";
    import About from "./components/About.vue";
    import Team from "./components/Team.vue";
    import OurProduct from "./components/OurProduct.vue";
    import Gallery from "./components/Gallery.vue";

    export default {
        components: {
            Hero,
            About,
            Team,
            OurProduct,
            Gallery,
        },
    };
</script>

<template>
    <Hero />
    <About />
    <Team />
    <OurProduct />
    <Gallery />
</template>
