<template>
   <main>
        <!--  content -->
        <section class="content">
            <div class="container">
                <div class="current-series-text btn">
                    current series
                </div>

                <div class="cards-container d-flex">
                    <DcSeriesCard v-for="card, index in dcSeries" :key="index" :seriesDetails="card"/>
                </div>

                <div class="d-flex">
                    <span class="load-more btn">
                        <a href="#">LOAD MORE</a>
                    </span>
                </div>

            </div>
        </section>

        <!-- buy links -->
        <section class="buy-links">
            <div class="container">

                <!-- buy links content -->
                <ul class="d-flex">
                    <li v-for="(link, index) in buyLinks" :key="index">
                        <a :href="link.url" class="d-flex">

                            <!-- icon -->
                            <div class="icon">
                                <img :src="link.image" :alt="link.text">
                            </div>
                            
                            <!-- text -->
                            <div class="text">
                                <span> {{ link.text }} </span>
                            </div>
                        </a>
                    </li>
                </ul>

            </div>
        </section>
   </main>
</template>

<script>
import DcJsonSeries from '../assets/dc-comics.json'
import DcSeriesCard from './DcSeriesCard.vue'

export default {
    name: "DcMain",
    components: {
        DcSeriesCard
    },
    data() {
        return {
            dcSeries: DcJsonSeries,
            buyLinks: [
                {
                    text: 'digital comics',
                    image: require('../assets/img/buy-comics-digital-comics.png'),
                    url: '#'
                },
                {
                    text: 'dc merchandise',
                    image: require('../assets/img/buy-comics-merchandise.png'),
                    url: '#'
                },
                {
                    text: 'subscriptions',
                    image: require('../assets/img/buy-comics-subscriptions.png'),
                    url: '#'
                },
                {
                    text: 'shop locator',
                    image: require('../assets/img/buy-comics-shop-locator.png'),
                    url: '#'
                },
                {
                    text: 'dc power visa',
                    image: require('../assets/img/buy-dc-power-visa.svg'),
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

main {
    color: white;

    .content {
        padding: 40px 0;
        background-color: $dc-main-primary-color;  

        .container {
            font-size: 25px;
            position: relative;
            
            .btn {
                background-color: $dc-main-secondary-color;
                font-size: 18px;
                font-weight: bold;
                text-transform: uppercase;
            }

            .current-series-text {
                position: absolute;
                top: -55px;
                left: 0;
                padding: 5px 16px;
            }

            .cards-container {
                flex-wrap: wrap;
                justify-content: space-between;
            }

            .d-flex {
                justify-content: center;

                .load-more {
                    padding: 7px 40px;
                    font-size: 12px;
                }
            }
           
        }
    }

    .buy-links {
        padding: 40px 0;
        background-color: $dc-main-secondary-color;
        
        .container {
            width: 65%;

            ul {
                align-items: center;
                justify-content: space-between;

                a {
                    align-content: center;

                    img {
                        height: 45px; 
                        margin-right: 8px;
                    }

                    span {
                        line-height: 45px;
                        font-size: 11px;
                        text-transform: uppercase;
                    }

                }

                li:last-child img {
                    padding-top: 5px;
                    width: 50px;
                    height: auto;
                }
            }
        }

        
    }
}
</style>