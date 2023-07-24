<script>
    export default {
    data() {
        return {
        
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
            <div class="container">
                <!-- <div>
                    <i class="fa-solid fa-chevron-left"></i>
                </div>

                <div>
                    <i class="fa-solid fa-chevron-right"></i>
                </div> -->
                <div class="row justify-content-center">
                    <div class="col-4">
                        <h1>
                            Devotion that never <em><strong>ends</strong></em>
                        </h1>
                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis tempore at architecto est impedit nostrum vitae quasi voluptates similique consequatur.
                        </p>
                        <button>
                            read more
                        </button>
                            
                    </div>
    
                    <div class="col-4">
                        
                    
                        <img src="../assets/img/h-2-slider-img-15.png" alt="">
                    
                    
                        <img src="../assets/img/h-2-slider-img-16.png" alt="">
                    
                    
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
    }
    li {
        list-style:none;
        padding-left: 10px;
        display: inline-block;
        
        > a {
            text-decoration: none;
            color: black;
        }
    }
</style>