<template>
    <header>
        
        <!-- container -->
        <div class="container d-flex">
            <!-- header logo -->
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="logo">
            </div>
            
            <!-- navigation menu -->
            <nav>
                <ul class="menu d-flex">
                    <!-- ciclo for che stampa nel dom i link di menuLinks -->
                    <li v-for="(link, index) in menuLinks" :key="index" :class="{ 'current': link.current }">
                        <a :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>

    </header>
</template>

<script>
export default {
    name: "DcHeader",
    data() {
        return {
            menuLinks: [
                {
                    text: 'characters',
                    url: '#',
                    current: false     
                },
                {
                    text: 'comics',
                    url: '#',
                    current: true
                },
                {
                    text: 'movies',
                    url: '#',
                    current: false
                },
                {
                    text: 'tv',
                    url: '#',
                    current: false
                },
                {
                    text: 'games',
                    url: '#',
                    current: false
                },
                {
                    text: 'collectibles',
                    url: '#',
                    current: false
                },
                {
                    text: 'videos',
                    url: '#',
                    current: false
                },
                {
                    text: 'fans',
                    url: '#',
                    current: false
                },
                {
                    text: 'news',
                    url: '#',
                    current: false
                },
                {
                    text: 'shop',
                    url: '#',
                    current: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

    header {
        background-color: white;
        height: 80px;
        
        .d-flex {
            justify-content: space-between;
            align-items: center;

            .logo {
                width: 35%;

                img {
                    width: 65px;
                }
            }

            nav {
                width: 65%;
                line-height: 70px;

                li {
                    margin: 0 10px;

                    a {
                        text-transform: uppercase;
                        font-size: 13px;
                        font-weight: bold;
                    }
                
                    &.current {
                        border-bottom: 5px solid $dc-main-secondary-color;
                        padding-top: 5px;
                    }    
                }
            }
        }
    }
</style>