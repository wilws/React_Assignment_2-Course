<template>
    <div class="space">
        <button v-if="rotateDeg > forwardButtonAppearDeg && rotateDeg < 0" class="forward" @click="rotate('forward')"><i  :style="{ color:buttonSetting.backgroundColor}" class="fa-solid fa-angle-left"></i></button>
        <button v-if="rotateDeg < 0"  class="backward" @click="rotate('backward')"><i :style="{ color:buttonSetting.backgroundColor}" class="fa-solid fa-angle-left"></i></button>
        <button v-if="rotateDeg < 0"  class="firstPage" @click="rotate('firstPage')"><i :style="{ color:buttonSetting.backgroundColor}" class="fa-solid fa-house"></i></button>
       <div class="box">
            <div v-if="hasSlot1" class="face1"><slot name="slot1"></slot></div>
            <div v-if="hasSlot3" class="face2"><slot name="slot3"></slot></div>
            <div v-if="hasSlot4" class="face3"><slot name="slot4"></slot></div>
            <div v-if="hasSlot2" class="face4"><slot name="slot2"></slot></div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            rotateDeg : 0,
            forwardButtonAppearDeg : 0,
            hasSlot1 :false,
            hasSlot2 :false,
            hasSlot3 :false,
            hasSlot4 :false,
            buttonSetting : { 
                backgroundColor : "white",
                color:"Black",
            },
            boxClass : "",    // to pin in the targeted box to rotate if this slot is repeated used
            animationClass:{  // to trigger animation
                'slot1':[],
                'slot2':[],
                'slot3':[],
                'slot4':[],
            },
       }
    },

    created(){
        // check if slot is inserted. 
        // for those slot has nth to be inserted, disappearing it by v-if
        this.hasSlot1 = (this.$slots.slot1) ? true:false;
        this.hasSlot2 = (this.$slots.slot2) ? true:false;
        this.hasSlot3 = (this.$slots.slot3) ? true:false;
        this.hasSlot4 = (this.$slots.slot4) ? true:false;

        
        this.buttonVisibilityController();
        

    },
    mounted(){

        // Responsive Setting
        // this.resizeAdjustor();                          
        window.addEventListener("resize",this.resizeAdjustor);    // Always ready to trigger "resize()" when width change. 
    },

    methods:{
        rotate(direction){   
            if (!this.singlePageChecker()) {   // [ Disallow this action ]: Check if it is just 1 page i.e only slot 1 or no slot at all. if yes, leave the function
                return
            }
            switch(direction) {
                case "forward":
                    this.rotateDeg -= 90;
                    break;
                case "backward":
                    this.rotateDeg += 90;
                    break;
                case "firstPage":
                    this.rotateDeg = 0;
                    break;
                default:
                    break;
            }
            document.querySelector(this.boxClass).style.transition = "transform 1s";  // When rotate browser, we want to see the rotation
            this.rotateController();      
        },
        resizeAdjustor(){
            document.querySelector(this.boxClass).style.transition = "transform 0s";   // When resize browser, we dont what the delay effect. It stop the transition delay when resize
            this.rotateController();                                          
        },

        mainScrollBarLocker(n){
            if(n){
                document.querySelector('html').style.overflow = 'hidden';
            } else {
                document.querySelector('html').style.overflow = 'scroll';
            }
        },

        rotateController(){
            const vw = Math.max(document.documentElement.clientWidth || 0, window.innerWidth || 0);
            const translateZ = `-${vw/2}px`;
            document.querySelector(this.boxClass).style.transform = `translateZ(${translateZ}) rotateY(${this.rotateDeg}deg) `;
    
            if (!this.rotateDeg){      
                 this.animationClassRemover();     // remove animation when go back to first page
                 this.mainScrollBarLocker(false);
            } else {
                this.mainScrollBarLocker(true)
                this.animationClassController(this.rotateDeg);
            }
        },

        animationClassController(n){
    
            let classList = []
            switch(n){
                // case 0:
                //     break
                case -90:
                    classList = this.animationClass.slot2;
                    break;
                case -180:
                    classList = this.animationClass.slot3;
                    break;
                case -270:
                    classList = this.animationClass.slot4;
                    break
            }
            this.animationClassInserter(classList);
        },

        animationClassInserter(n){
            n.forEach((c) => {
                document.querySelector(c).classList.add('animation');
            });
        },
        animationClassRemover(){

            document.querySelectorAll('.animation').forEach((c) => {
                c.classList.remove('animation');
            })
            
        },

        singlePageChecker(){
            // check if it is just 1 page i.e only slot 1 or no slot at all. if yes, disable forward/backward function
            if (!this.hasSlot1 && !this.hasSlot2 && !this.hasSlot3 && !this.hasSlot4){
                return false
            }

            if (this.hasSlot1 && !this.hasSlot2 && !this.hasSlot3 && !this.hasSlot4){
                return false
            }
            return true
        },

        buttonVisibilityController(){

            if (this.hasSlot2){
                this.forwardButtonAppearDeg = -90;
            }

            if (this.hasSlot3){
                this.forwardButtonAppearDeg = -180;
            }

            if (this.hasSlot4){
                this.forwardButtonAppearDeg = -270;
            }
        },
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
    position: relative;
    width:100%;
    height:100%;
   
    background-color: rgb(236, 231, 231);
    perspective: $perspective;
    @include vertical-horizontal-center();
}

@mixin buttonStyle {
        position:absolute;
        background-color: transparent;
        border:none;
        top:0;
        // left:0rem;
        width:1.5rem;
        height:100%;
        z-index: 3;
        transition-property:background-color transform ;
        transition-duration: .5s;
        cursor: pointer;

        @media(min-width:768px){
            width:2rem;
        }
        @media(min-width:1024px){
            width:2.2rem;
        }

        i{
            font-size: 1.3rem;
            @media(min-width:768px){
                font-size: 2rem;
            }
            @media(min-width:1024px){
                font-size:2.2rem;
            }
        }

    &:hover{
        background-color: rgba(255, 255, 255, 0.1);
    }
}

.backward{
    @include buttonStyle();
    left:0rem;
    &:hover{
        background-color: rgba(255, 255, 255, 0.1);
        transform:scale(1.5);
    }
}

.forward{
    @include buttonStyle();
    transform:rotateZ(180deg);
    right:0rem;
    &:hover{
        background-color: rgba(255, 255, 255, 0.1);
        transform:rotateZ(180deg) scale(1.5);
    }
}


.firstPage{
    position:absolute;
    top:1rem;
    right:1rem;
    border: none;
    background-color: transparent;
    z-index: 10;
    transition-property:background-color transform ;
    transition-duration: .5s;
    font-family: $tertiary-font;
    cursor: pointer;

    i{
        font-size: 1.3rem;
        @media(min-width:768px){
            font-size: 1.7rem;
        }
        @media(min-width:1024px) and (max-height:1024px){
            font-size:1.6rem;
        }

        @media(min-width:1024px) and (min-height:1024px){
            font-size:2.2rem;
        }
    }
    
    &:hover{
        background-color: rgba(255, 255, 255, 0.1);
        transform: scale(1.1);
    }
}



.box{
    position:relative;
    width:$boxWidth;
    height:$boxHeight;
    // transform: translateZ(-$translateDistanceFront) rotateY(-270deg);
    transform: translateZ(-$translateDistanceFront);
    transform-style: preserve-3d;
    transform-origin: center;


    @mixin setting{
        position:absolute;
        padding: 0;
        margin: 0;
        top:0;
        left:0;
        width:100%;
        height:100%;
        transform-origin: center;
        @include vertical-horizontal-center();
    }

    .face1{
        @include setting();
        transform: translateZ($translateDistanceFront);
        background-color: white;
    }
    .face2{
        @include setting();
        transform: translateZ($translateDistanceBack) rotateY(180deg);
        background-color: white;
    }
    .face3{
        @include setting();
        transform: translateX($translateDistanceLeft) rotateY(-90deg) ;
        background-color: white;
    }
    .face4{
        @include setting();
        // color:white;
        transform: translateX($translateDistanceRight) rotateY(90deg) ;
        background-color: white;
    }
}

</style>