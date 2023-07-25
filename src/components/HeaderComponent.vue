<script>
    import {store} from '../store.js'
    export default {
        data() {
            return {
                store,

                images: [
                    {
                        leftImage: 'h-2-slider-img-15.png',
                        rightImage:'h-2-slider-img-16.png',
                        secondaryImageOne:'h-2-slider-img-12.png',
                        secondaryImageTwo:'h-2-slider-img-13.png',
                        secondaryImageThree:'short-slider-rev-1-img-2.png',
                        secondaryImageFour:'h-2-slider-img-14.png',
                        secondaryImageFive:'short-slider-rev-1-img-6.png',
                        secondaryImageSix:'h-2-slider-img-17.png',
                        title:'Devotion that never ends',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis tempore at architecto est impedit nostrum vitae quasi voluptates similique consequatur.',
                        slideButton:'read more'
                    },
                    {
                        leftImage: 'short-slider-rev-1-img-3.png',
                        rightImage:'h-2-slider-img-11.png',
                        secondaryImageOne:'short-slider-rev-1-img-1.png',
                        secondaryImageTwo:'h-2-slider-img-13.png',
                        secondaryImageThree:'short-slider-rev-1-img-4.png',
                        secondaryImageFour:'short-slider-rev-1-img-5.png',
                        secondaryImageFive:'short-slider-rev-1-img-10.png',
                        secondaryImageSix:'short-slider-rev-1-img-9.png',
                        title:'Devotion that never ends',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis tempore at architecto est impedit nostrum vitae quasi voluptates similique consequatur.',
                        slideButton:'read more'
                    }
                ],
                slideIndex: 0,


            }
        },
        methods: {
            getImage: function(img) {
                return new URL(`../assets/img/${img}` , import.meta.url).href;
            },
            nextSlide(){
                this.slideIndex++;
            },
            prevSlide(){
                this.slideIndex--;
            }
        }
    }
</script>


<template>
    <Header>
        <section>
            
            <div class="row justify-content-between align-items-center p-2">
                 <div class="col-auto">
                     <img class="logo" src="../assets/img/logo-sidearea-1.png" alt="Marèe">
                 </div>
     
                <div class="col-auto">
                    <div class="row align-items-center">
                        <div class="col-auto">
                            <ul class="">
                               <li>
                                    <a href="#">
                                        HOME
                                    </a>
                               </li>
                               <li>
                                    <a href="#">
                                        PAGES
                                    </a>
                               </li>
                               <li>
                                    <a href="#">
                                        PORTFOLIO
                                    </a>
                               </li>
                               <li>
                                    <a href="#">
                                        BLOG
                                    </a>
                               </li>
                               <li>
                                    <a href="#">
                                        SHOP
                                    </a>
                               </li>
                               <li>
                                    <a href="#">
                                        ELEMENTS
                                    </a>
                               </li>
                            </ul>
                        </div>
                        <div class="col-auto">
                            <div>
                                <a href="#">
                                    
                                    <img src="../assets/svg/svg-1.svg" alt="">
                                </a>
                            </div>
                            
                            
                            
                        </div>

                    </div>

                            
                </div>
            </div>
        </section>

        <section>
            <div class="container mt-5">
                <div class="slider-box">
                    <div class="prev" @click="prevSlide()">
                       <i class="fa-solid fa-chevron-left"></i>
                   </div>
                    <div class="next" @click="nextSlide()">
                        <i class="fa-solid fa-chevron-right"></i>
                    </div>
                    <div class="row justify-content-center align-items-center" v-for="(image, index) in images" :key="index" :class="index == slideIndex ? '' : 'none'" >
                        <div class="col-5">
                            <div class="slide-description">
                                <h1>
                                   {{ images[slideIndex].title }} 
                                </h1>
                                <p>
                                    {{ images[slideIndex].description }}
                                </p>
                                <button>
                                    {{ images[slideIndex].slideButton }}
                                </button>
                                
                            </div>

                                
                        </div>
        
                        <div class="col-6">
                            
                            <div class="img-slider d-flex justify-content-center" >
                                <div class="img-box">

                                    <img :src="getImage(images[slideIndex].leftImage)" alt="">
                                    
                                    <div class="secondary-img first">
                                        <img :src="getImage(images[slideIndex].secondaryImageOne)" alt="">
                                    </div>
    
                                    <div class="secondary-img second">
                                        <img :src="getImage(images[slideIndex].secondaryImageTwo)" alt="">
                                    </div>
    
                                    <div class="secondary-img third">
                                        <img :src="getImage(images[slideIndex].secondaryImageThree)" alt="">
                                    </div>
                                </div>
                                    

                                <div class="img-box">

                                    <img :src="getImage(images[slideIndex].rightImage)" alt="">

                                    <div class="secondary-img fourth">
                                        <img :src="getImage(images[slideIndex].secondaryImageFour)" alt="">
                                    </div>
    
                                    <div class="secondary-img fifth">
                                        <img :src="getImage(images[slideIndex].secondaryImageFive)" alt="">
                                    </div>

                                    <div class="secondary-img sixth">
                                        <img :src="getImage(images[slideIndex].secondaryImageSix)" alt="">
                                    </div>
                                </div>

                            </div>
                                    
                            
                        
                        
                        </div>
                    </div>
                </div>
            </div>
        </section>
                    
                            
    </Header>
</template>

<style scoped lang="scss">
    .logo {
        padding-left: 10px;
        vertical-align: middle;
        
    }
    ul {
        vertical-align: middle;
        display: inline;
        li {
            list-style:none;
            padding-left: 10px;
            display: inline-block;
            
            > a {
                text-decoration: none;
                color: black;
            }
        }
    }
    .none {
        display: none;
    }
    
    .img-slider{
        
        .img-box {
            width: 200px;
            display: inline-block;
            position: relative;
            
          
        }
        .secondary-img {
           
          width: 30px;
          position: absolute;
       }
    
       .first {
           bottom: 50%;
           right: 100%;
        }
           
       .second {
           bottom: 10%;
           left:0;
       }

       .third {
           bottom: 100%;
           left: 10%;
        }
        
        .fourth {
            bottom: 100%;
            right: 10%;
        }
        .fifth {
            bottom: 50%;
            left: 100%;
        }

        .sixth {
            bottom: 10%;
            right: 0;
        }

    }

    .slider-box {
        position: relative;
        > .prev {
            position: absolute;
            top: 50%;
            right: 100%;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            line-height: 30px;
            text-align: center;
            background-color: #F5D8CA;

            > i {
                
                color: white;
            }
            
        }

        > .next {
            position: absolute;
            left: 100%;
            top: 50%;
            width: 30px;
            height: 30px;
            line-height: 30px;
            border-radius: 50%;
            text-align: center;
            background-color: #F5D8CA;

            > i {
                
                color: white;
            }
            
        }
    }


</style>