<template>
    <div class="serie-card">
        <img :src="seriesDetails.thumb" :alt="seriesDetails.series">
        <h2>{{ seriesDetails.series }}</h2>
    </div>
</template>

<script>
export default {
    name: "DcSeriesCard",
    props: {
        seriesDetails: Object
    }
}
</script>

<style lang="scss" scoped>
.serie-card {
    width: calc( (100% / 6) - 30px );
    margin: 15px;

    img {
        height: 185px;
        width: 100%;     
        object-fit: cover;
        object-position: top;
        margin: 15px 0;
    }
}

h2 {
    font-size: 14px;
}
</style>