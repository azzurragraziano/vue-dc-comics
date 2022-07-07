<template>
    <div class="serie-card">
        <a href="#">
            <img :src="seriesDetails.thumb" :alt="seriesDetails.series">
            <h2>{{ seriesDetails.series }}</h2>
        </a>
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
        height: 150px;
        width: 150px;
        overflow: hidden;     
        object-fit: cover;
        object-position: top;
        margin: 15px 0;
    }

    h2 {
        font-size: 11px;
        text-transform: uppercase;
        font-weight: 400;
    }
}
</style>