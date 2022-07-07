<template>
    <footer>
        <!-- footer top (con bg-image) -->
        <div class="footer-top">
            <div class="container d-flex">

                <!-- links list -->
                <div class="footer-col-list d-flex">

                    <!-- left list col -->
                    <ul class="left-list-col">

                        <!-- footer dc comics list -->
                        <li v-for="(links, index) in footerDcComicsList" :key="index">
                            
                            <!-- list title -->
                            <div class="list-title">
                                {{ links.title }}
                            </div>

                            <!-- link list -->
                            <ul>
                                <li class="link-list" v-for="(element, index) in footerDcComicsList[index].linksList" :key="index" >
                                    <a href="links.url">
                                        {{ element.link }}
                                    </a>
                                </li>
                            </ul>
                        </li>

                        <!-- footer shop list -->
                        <li v-for="(links, index) in footerShopList" :key="index">
                            
                            <!-- list title -->
                            <div class="list-title">
                                {{ links.title }}
                            </div>

                            <!-- link list -->
                            <ul>
                                <li class="link-list" v-for="(element, index) in footerShopList[index].linksList" :key="index" >
                                    <a href="links.url">
                                        {{ element.link }}
                                    </a>
                                </li>
                            </ul>
                        </li>
                    </ul>

                    <!-- central list col -->
                    <ul class="central-list-col">

                        <!-- footer dc comics list -->
                        <li v-for="(links, index) in footerDcList" :key="index">
                            
                            <!-- list title -->
                            <div class="list-title">
                                {{ links.title }}
                            </div>

                            <!-- link list -->
                            <ul>
                                <li class="link-list" v-for="(element, index) in footerDcList[index].linksList" :key="index" >
                                    <a href="links.url">
                                        {{ element.link }}
                                    </a>
                                </li>
                            </ul>
                        </li>

                    </ul>

                    <!-- right list col -->
                    <ul class="right-list-col">

                        <!-- footer dc comics list -->
                        <li v-for="(links, index) in footerSitesList" :key="index">
                            
                            <!-- list title -->
                            <div class="list-title">
                                {{ links.title }}
                            </div>

                            <!-- link list -->
                            <ul>
                                <li class="link-list" v-for="(element, index) in footerSitesList[index].linksList" :key="index" >
                                    <a href="links.url">
                                        {{ element.link }}
                                    </a>
                                </li>
                            </ul>
                        </li>

                    </ul>

                </div>

                <!-- logo bg-image -->
                <div class="logo-bg-img"></div>

            </div>
        </div>

        <!-- footer bottom -->
        <div class="footer-bottom">
            <div class="container d-flex">

                <!-- sign up btn -->
                <div class="btn">
                    sign-up now!
                </div>
                
                <!-- social links list -->
                <ul class="d-flex">

                    <li class="title">
                        follow us
                    </li>

                    <li>
                        <a href="#">
                            <img src="../assets/img/footer-facebook.png" alt="">
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <img src="../assets/img/footer-twitter.png" alt="">
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <img src="../assets/img/footer-youtube.png" alt="">
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <img src="../assets/img/footer-pinterest.png" alt="">
                        </a>
                    </li>

                    <li>
                        <a href="#">
                            <img src="../assets/img/footer-periscope.png" alt="">
                        </a>
                    </li>
                </ul>

            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "DcFooter",
    data() {
        return {
            footerDcComicsList: [
                {
                    title: 'DC COMICS',
                    url: '#',
                    linksList: [
                        {
                            link: 'Characters'
                        },
                        {
                            link: 'Comics'
                        },
                        {
                            link: 'Movies'
                        },
                        {
                            link: 'TV'
                        },
                        {
                            link: 'Games'
                        },
                        {
                            link: 'Videos'
                        },
                        {
                            link: 'News'
                        }
                    ]   
                }
            ],
            footerShopList: [
                {
                    title: 'SHOP',
                    url: '#',
                    linksList: [
                        {
                            link: 'Shop DC'
                        },
                        {
                            link: 'Shop DC Collectibles'
                        }
                    ]   
                }
            ],
            footerDcList: [
                {
                    title: 'DC',
                    url: '#',
                    linksList: [
                        {
                            link: 'Terms Of Use'
                        },
                        {
                            link: 'Privacy policy (New)'
                        },
                        {
                            link: 'Ad Choices'
                        },
                        {
                            link: 'Advertising'
                        },
                        {
                            link: 'Jobs'
                        },
                        {
                            link: 'Subscriptions'
                        },
                        {
                            link: 'Talent Workshops'
                        },
                        {
                            link: 'CPSC Certificates'
                        },
                        {
                            link: 'Ratings'
                        },
                        {
                            link: 'Shop Help'
                        },
                        {
                            link: 'Contact Us'
                        }
                    ]   
                }
            ],
            footerSitesList: [
                {
                    title: 'SITES',
                    url: '#',
                    linksList: [
                        {
                            link: 'DC'
                        },
                        {
                            link: 'MAD Magazine'
                        },
                        {
                            link: 'DC Kids'
                        },
                        {
                            link: 'DC Universe'
                        },
                        {
                            link: 'DC Power Visa'
                        }
                    ]   
                }
            ]
        }
    }  
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    
 .d-flex {
    justify-content: space-between;

    .footer-col-list {
        padding-top: 35px;

        &>* {
            padding-right: 25px;

            .list-title {
                color: $dc-font-primary-color;
                font-weight: bold;
                margin: 15px 0;
            }

            .link-list {
                color: gray;
                font-size: 12px;
                padding-bottom: 5px;
            }
        }
    }   

    div.logo-bg-img{
        height: 370px;
        width: 560px;
        background-image: url('../assets/img/dc-logo-bg.png');
        background-size: cover;
        background-position: center;
    }
 }
}

.footer-bottom {
    background-color: #242424;
    padding: 30px 0;

    .d-flex {
        justify-content: space-between;

        .btn {
            text-transform: uppercase;
            border: 2px solid $dc-main-secondary-color;
            padding: 8px;
            color: white;
            font-weight: bold;
        }

       ul {
        align-items: center;

        li {
            margin-right: 15px;

            &.title {
                text-transform: uppercase;
                font-weight: bold;
                font-size: 18px;
                color: $dc-main-secondary-color;
            }

            img {
                width: 30px;
            }
        }
       }
    }
}

</style>