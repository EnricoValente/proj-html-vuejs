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
            
    </main>
</template>

<style scoped lang="scss">

</style>