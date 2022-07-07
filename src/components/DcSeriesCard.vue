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
        width: 100%;
        aspect-ratio: 1/1;   
        object-fit: cover;
        object-position: top;
        margin: 15px 0;
    }

    h2 {
        font-size: 0.7rem;
        text-transform: uppercase;
        font-weight: 400;
    }
}
</style>