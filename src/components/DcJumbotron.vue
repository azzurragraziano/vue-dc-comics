<template>
    <section class="jumbotron">
        <!-- <img :src="imgSrc" alt="jumbotron"> -->
    </section>
</template>

<script>
export default {
    name: "DcJumbotron",
    data() {
        return {
            // imgSrc: require('../assets/img/jumbotron.jpg')
        }
    }
}
</script>

<style lang="scss" scoped>
section {
    height: 350px;
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: cover;
    background-repeat: no-repeat;
}
</style>