<script>
export default {
    name: 'MyJumbo',
    data: () => ({
        image_name: 'lucca_concert.jpeg'
    }),
    methods: {
        createImagePath(image_name) {
            const url = new URL(`../assets/img/${image_name}`, import.meta.url);
            return url.href;
        }
    }
}
</script>

<template>
    <figure>
        <img :src="createImagePath(image_name)" alt="lucca concert">
    </figure>
    <figure>
        <img src="../assets/img/rolling-stones.jpeg" alt="rolling stones">
    </figure>
</template>

<style></style>