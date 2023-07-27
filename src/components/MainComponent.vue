<script>
    import { store } from '../store';
    export default {
    data() {
        return {
            store,
            portCards: [
                {
                    src: 'h-2-port-img-1.jpg'
                },
                {
                    src: 'h-2-port-img-2.jpg'
                },
                {
                    src: 'h-2-port-img-3.jpg'
                },
                {
                    src: 'h-2-port-img-4.jpg'
                },
                {
                    src: 'h-2-port-img-5.jpg'
                },
                {
                    src: 'h-2-port-img-6.jpg'
                },
            ],
            icons: [
                {
                    class:'fa-solid fa-lightbulb',
                    title:'First theres an idea',
                    description:' Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.'
                },
                {
                    class:'fa-regular fa-comment',
                    title:'Than we talk about',
                    description:' Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.'
                },
                {
                    class:'fa-solid fa-cloud',
                    title:'And we think about',
                    description:' Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.'
                },
                {
                    class:'fa-solid fa-compass-drafting',
                    title:'So we draw along',
                    description:' Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.'
                },
            ]
        }
    },
    methods: {
        getImagePath: function(src) {
            return new URL(`../assets/img/${src}` , import.meta.url).href;
            
        }
    }
}
</script>


<template>
    <main class="mt-4">
        <section>
            <div class="row">
              <div class="col-4 g-0" v-for="(singleCard, i) in portCards" :key="i">
                <img :src="getImagePath(singleCard.src)" alt="">
              </div>
            </div>
        </section>
        
        <section class="bg-white">
            
            <div class="container">
                <h2 class="text-center pt-5">
                    Working process
                </h2>

                
                <div class="content-box py-3 mx-auto">
                    <div class="row justify-content-between">
                        <div class="process-box col-3 " v-for="(icon, index) in icons" :key="index">
                            
                                
                            <div class="icons text-center mx-auto">
                                <i :class="icon.class"></i>
                            </div>
    
                            <div class="text-center">
                                <h6>
                                    {{ icon.title }}
                                </h6>
                                <p>
                                    {{ icon.description }}
                                </p> 
    
                            </div>
                            
    
                        </div>
    
                    </div>

                </div>   
            </div>
                
        </section>
                    
                
                    
                
            
                    
                        
                
                    
                    
                    
                    
                    
                

        <section class="work-section pt-5">
            <div class="container">
                
                <div class="text-center col pt-5">
                    <h2>
                        Want to work with us? Send a message!
                    </h2>

                </div>
                <div class="text-center  pt-5">
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod amet quia rem corporis, perferendis labore nisi tenetur repellendus itaque saepe a ut iusto est error perspiciatis laborum sunt quaerat incidunt!
                    </p>
                </div>

                <div class="text-center pt-3 pb-5 link-container">
                    <button class="contact-link">
                        <a href="#" class="">CONTACT</a>
                    </button>

                </div>

               
                
                    
                    
                    

                
            </div>

        </section>

                        

                    
    </main>
</template>

<style scoped lang="scss">
    .content-box {
        background-image: url('../assets/svg/svg-3.svg');
        background-size: contain;
        background-repeat: no-repeat;
        max-width: 800px;
        
    }
        
        
        
    
        

    .icons {
        width: 80px;
        height: 80px;
        line-height: 90px; 
        background-color:#FAF7F1;
        border-radius: 50%;
        

        > i {
        font-size: 20px;
        
        }
        
        
        
    }
    .process-box {
            
        h6 {
            white-space: nowrap;
            font-size: 10px;
            
        }
    
        p {
            font-size: 10px;
            color: #A6A6A6;
            white-space: wrap;
            
        }
            
    }
    .work-section {
        background-image:url('../assets/img/h-2-background-1.jpg') ;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;

        .link-container {
            
            
           
            .contact-link {
                width: 110px;
                height: 40px;
                background-color: #D8F0E3;
                text-decoration: none;
                border: 1px solid #D8F0E3;
                
                > a {
                    font-size: 10px;
                    text-decoration: none;
                    color: black;
                    
                    
                }
               
            }

        }
        
    }        
        
        
             
            
        
    
        


</style>