<template>
    
    <div class="col-lg-6 col-md-7  d-none d-md-block h-100  carousel_container" :style="`background-image: url(${bgImage[count]})`">   
        <div class="card_container " >   
            <div class="text_img">
                We move 10x faster than our peers and syau consistent. While they're bogged down with design debt,<br>
                we're relasing new features.
            </div>
            <div class="my-3 d-flex justify-content-between">
                <div id="name_img">
                    Sophie Hall
                </div>
                <div class="star_container">
                    <img  v-for="i in 5" :key="i" src="../assets/img/star.svg" alt="">
                </div>
            </div>
            <div class=" d-flex justify-content-between align-items-center">
                <div class="job_description">
                    <span class="">Founder, Catalog</span>
                    <br>
                    <span>Web Design Agency</span>
                </div>
                <div id="arrows_box">
                    <img @click="prevImg(), stop()" class="arrow" src="../assets/img/arrow-l.svg" alt="">
                    <img @click="nextImg(), stop()" class="arrow  ms-4" src="../assets/img/arrow-r.svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"Carousel",
    data(){
        return{
        time:null,
        count:0,
        bgImage:[require("../assets/slideshow/1.jpeg"),require("../assets/slideshow/2.jpeg"),require("../assets/slideshow/3.jpeg")],
        }
    },
    mounted: function() {
        this.time=setInterval(()=>this.nextImg() , 2000);
    },
    methods:{
        nextImg(){
            this.count++
            if( this.count >= this.bgImage.length){
                this.count = 0;              
                
            }
        },
        prevImg(){
            this.count--;
            if(this.count == -1){
                this.count = this.bgImage.length-1; 
            }
        },
        stop: function() {
            clearInterval(this.time);
            this.time=setInterval(()=>this.nextImg() , 2000);
        }
    }
}
</script>

<style lang="scss" scoped>
    .carousel_container{
        height: 100%;
        overflow-y: auto;
        background-size: cover;
        background-position:center ;
    
        .card_container{
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            height: 100%;
            margin: 0;
            color: white;
            background-size: cover;
            background-position:center ;
            padding: 2rem 3.125rem;
            .text_img,#name_img{
                
                font-size: 1.5rem;
                font-weight: 400;
                text-align: start;
            }
            .star_container{
                img{
                    width:1.25rem; 
                    
                } 
            }
            .arrow{

                border: 1px solid white;
                border-radius: 50%;
                width: 3rem;
                padding: 0.6rem;
            }
            .arrow:hover{
                cursor: pointer;
            }
            .job_description {
                span{
                    font-size: .75rem;
                }
                span:last-child{
                font-weight: 300;
                font-size: .65rem;

                }
            }
        }
    }

</style>

