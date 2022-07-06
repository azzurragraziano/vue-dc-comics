<template>
   <main>
        <!--  content -->
        <section class="content">
            <div class="container">
                --> content goes here 
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
export default {
    name: "ProductsList",
    data() {
        return {
            buyLinks: [
                {
                    text: 'digital comics',
                    image: require('../assets/img/buy-comics-digital-comics.png'),
                    url: '#'
                    //40
                },
                {
                    text: 'dc merchandise',
                    image: require('../assets/img/buy-comics-merchandise.png'),
                    url: '#'
                    //50
                },
                {
                    text: 'subscriptions',
                    image: require('../assets/img/buy-comics-subscriptions.png'),
                    url: '#'
                    //52
                },
                {
                    text: 'shop locator',
                    image: require('../assets/img/buy-comics-shop-locator.png'),
                    url: '#'
                    // height: 50px
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