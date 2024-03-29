<script>
    import MainPage from '../components/MainPage.vue';
    import ItemSlider from '../components/ItemSlider.vue'

    export default {
        name: "App",
        components: {
            MainPage,
            ItemSlider,
        },
    };
</script>

<template>
    <MainPage />
    <ItemSlider />

</template>