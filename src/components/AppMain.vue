<script>
export default {
    data() {
        return {
            items:[
                {
                    img:'/vue-dc-comics-1/img/buy-comics-digital-comics.png',
                    description: 'DIGITAL COMICS'
                },
                {
                    img:'/vue-dc-comics-1/img/buy-comics-merchandise.png',
                    description: 'DC MERCHANDISE'
                },
                {
                    img:'../../public/vue-dc-comics-1/img/buy-comics-subscriptions.png',
                    description: 'SUBSCRIPTION'
                },
                {
                    img:'/vue-dc-comics-1/img/buy-comics-shop-locator.png',
                    description: 'COMIC SHOP LOCATOR'
                },
                {
                    img:'/vue-dc-comics-1/img/buy-dc-power-visa.svg',
                    description: 'DC POWER VISA'
                },
                
            ]
        };
    },
    methods: {

    }
}
</script>

<template>
   <div class="container-top">
        <div class="top-main">
            <section>
                <div>
                    content goes here!
                </div>
            </section>
        </div>
    </div>
   <div class="container-bottom">
     <div class="bottom-main">
        <section>
            <div class="img-box" v-for="(elem, i) in items">
                <img :src="elem.img" alt="">
                <div>
                    {{ elem.description }}
                </div>
            </div>
        </section>
    </div>
   </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables.scss' as*;
    @use '../assets/scss/partials/reset.scss' as*;
   .container-top{
   
    width: $fullSpace;
    background-color: black;
        .top-main{
            width: $fullSpace;
            section{
                width: $containerSize;
                height: $sectionHeight;
                color: white;
                margin: 0 auto;
                font-size: 3rem;
            }
        }
    }
    .container-bottom{
        background-color: $dc-color;
        .bottom-main{
            width: $containerSize;
            margin: 0 auto;
                section{
                    widows: $fullSpace;
                    height: $sectionHeight;
                    display: flex;
                    align-items: center;
                    color: white;
                    .img-box{
                        width: calc(100% / 6);
                        margin-left: 20px;
                        display: flex;
                        align-items: center;
                        img{
                            width: 50px;
                            margin-right: 10px;
                        }
                    }
                }
            }
    }
</style>
                
    

