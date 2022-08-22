<template>
    <div class="space">
        <button v-if="rotateDeg >-270" class="forward" @click="rotate('forward')">Next</button>
        <button v-if="rotateDeg <= -90" class="backward" @click="rotate('backward')">Previous</button>
        <div class="box">
            <div class="face1"><slot name="face1"></slot></div>
            <div class="face2">face2</div>
            <div class="face3">face 3</div>
            <div class="face4">face 4</div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            rotateDeg : 0,
        }
    },
    methods:{
        rotate(direction){
            if ( direction === "forward"){
                this.rotateDeg -= 90;
            } else {
                this.rotateDeg += 90;
            }            
            this.resizeTranslateZ();
            const vw = Math.max(document.documentElement.clientWidth || 0, window.innerWidth || 0);
            const translateZ = `-${vw/2}px`;
            document.querySelector('.box').style.transform = `translateZ(${translateZ}) rotateY(${this.rotateDeg}deg) `;
            // document.querySelector('.box').style.transform = `rotateY(${this.rotateDeg}deg)`;
        },
        resizeTranslateZ(){
            const vw = Math.max(document.documentElement.clientWidth || 0, window.innerWidth || 0);
            const translateZ = `-${vw/2}px`;
            document.querySelector('.box').style.transform = `translateZ(${translateZ})`;

        }
    }

}
</script>

<style lang="scss" scoped>

$boxWidth : 100vw;
$boxHeight: 100vh;
$perspective: $boxWidth * 5;

$translateDistanceFront : $boxWidth/2;
$translateDistanceBack : -$boxWidth/2;
$translateDistanceLeft : -$boxWidth/2;
$translateDistanceRight : $boxWidth/2;

.space{
    width:100%;
    height:100%;
    position: relative;
    background-color: rgb(104, 95, 95);
    perspective: $perspective;
    @include vertical-horizontal-center();

}

.forward{
        position:absolute;
        top:0;
        right:0;
        width:3rem;
        height:3rem;
        z-index: 3;
}

.backward{
        position:absolute;
        top:0;
        left:0;
        width:3rem;
        height:3rem;
        z-index: 3;
}

.box{
    position:relative;
    width:$boxWidth;
    height:$boxHeight;
    // transform: rotateY(0deg) rotateX(0deg) rotateZ(0deg);
    transform: translateZ(-$translateDistanceFront);
    transform-style: preserve-3d;
    transition:transform 1s;
    transform-origin: center;


    @mixin setting{
        position:absolute;
        width:100%;
        height:100%;
        font-size: 5rem;
        transform-origin: center;
        @include vertical-horizontal-center();
    }

    .face1{
        @include setting();
        transform: translateZ($translateDistanceFront);
        background-color: red;
    }
    .face2{
        @include setting();
        transform: translateZ($translateDistanceBack) rotateY(180deg);
        background-color: blue;
    }
    .face3{
        @include setting();
        transform: translateX($translateDistanceLeft) rotateY(-90deg) ;
        background-color: rgb(64, 202, 179);
    }
    .face4{
        @include setting();
        color:white;
        transform: translateX($translateDistanceRight) rotateY(90deg) ;
        background-color: rgb(41, 8, 8);
    }
}

</style>