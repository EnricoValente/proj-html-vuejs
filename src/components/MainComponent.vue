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
                    title:'First theres an idea',
                    description:' Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.'
                },
                {
                    class:'fa-solid fa-cloud',
                    title:'First theres an idea',
                    description:' Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.'
                },
                {
                    class:'fa-solid fa-compass-drafting',
                    title:'First theres an idea',
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
    <main>
        <section>
            <div class="row">
              <div class="col-4 g-0" v-for="(singleCard, i) in portCards" :key="i">
                <img :src="getImagePath(singleCard.src)" alt="">
              </div>
            </div>
        </section>
        
        <section>
            
            <div class="container">
                <h2 class="text-center pt-5">
                    Working process
                </h2>
                <div class="row justify-content-between aling-items-center content-box pt-4">
                    <div class="process-box col-2" v-for="(icon, index) in icons" :key="index">
                        
                           
                        <div class="icons text-center">
                            <i :class="icon.class"></i>
                        </div>

                        
                        <!-- <h6 class="text-center">
                            First theres an idea
                        </h6>
                        <p class="text-center">
                            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur sequi laborum dolor perferendis vitae ad.
                        </p> -->
                        

                    </div>

                </div>
                    
                
            
                    
                        
                
            </div>
                    
                    
        </section>
                    
                    
                    
                

        <section>
            <h2>
                Working progress
            </h2>
        </section>
                    
    </main>
</template>

<style scoped lang="scss">
    .content-box {
        background-image: url('../assets/svg/svg-3.svg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        
    
    }
        

        .icons {
           width: 100px;
           height: 100px;
           line-height: 110px; 
           background-color:#FAF7F1;
           border-radius: 50%;
           

           > i {
            font-size: 30px;
           
           }
           
          
           
        }
        .icons-text {
            width: 200px;
        }
            
        h6 {
            white-space: nowrap;
        }

        p {
            font-size: 10px;
            color: #A6A6A6;
            white-space: wrap;
        }
             
            
        
    
        


</style>