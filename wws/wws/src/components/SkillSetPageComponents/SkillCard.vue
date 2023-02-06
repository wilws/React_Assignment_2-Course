<template>

    <!-- card 1 Front End-->
    <div class="card-wrapper">

        <div class="card" :id="id">

            <div class="card-title">
                <h3>{{ title }}</h3>
                <h4>{{ subtitle }}</h4>
            </div>

            <div class="card-tech-chart">

                <skill-item  
                    v-for="skill in skills" 
                    :key="skill.id"
                    :id="skill.id"
                    :IconImageSrc="skill.iconSrc"
                    :techName="skill.techName"
                    :bar="skill.bar"
                    :scrollToPage= scrollToPage
                >
                </skill-item>

            </div>
            <!-- end of card-tech-chart -->
        </div>
        <!-- End of card -->
    </div>
    <!-- End of card wrapper-->


</template>


<script>

import SkillItem from "./SkillItem.vue";
export default {
    components: { SkillItem },
    props:['skills', 'title', 'subtitle','id','scrollToPage','currentCard'],
    watch:{
        scrollToPage(value){
            if (value){
                this.cardsRotation(this.cardRotateDeg,500);
            } else {
                this.cardsRotation();
            }
        },
        currentCard(value){
            this.moveCard(value)
        }

    },
    data(){
        return {
            cardRotateDeg : -25, 
        }
    },
    methods:{
        moveCard(n){
            // [ small screen ] Moves cards-wrapper horizontally to display other cards 
            this.cardsRotation();
            const translateDistance = window.innerWidth * -n;
            document.querySelector('.cards-wrapper').style.transform = `translateX(${translateDistance}px)`;
            this.cardsRotation(this.cardRotateDeg,1000);
        },

        cardsRotation(deg=0,delayTime=0){
            // funtion that rotates the card.
            document.querySelectorAll('.card').forEach(card => {
                setTimeout(()=>{
                    card.style.transform = `rotateY(${deg}deg)`;
                },delayTime);
            })
        },
    }


    // data(){
    //     return {
    //         cardRotateDeg : -25,     // card rotation Y degree
    //         id: "#skill-set-page",
    //     }
    // },
    // mounted(){
    //     window.addEventListener('scroll',()=>{
    //         this.cardsScrollingRotateEffect();
    //     });
    //     // Check if the device is horizontally rotated 
    //     // if true, add class "rotated" to the <section> tag
    //     // We treat the style of the horizontal screen separately
    //     this.deviceRotationResponse(this.id)
    //     window.addEventListener('resize',()=>{
    //         this.deviceRotationResponse(this.id);
    //         this.moveCard(0);     // When screen change, need reposite back the card to the origin 
    //     });


    // },
    // methods:{
    //     moveCard(n){
    //         // [ small screen ] Moves cards-wrapper horizontally to display other cards 
    //         this.cardsRotation();
    //         const translateDistance = window.innerWidth * -n;
    //         document.querySelector('.cards-wrapper').style.transform = `translateX(${translateDistance}px)`;
    //         this.cardsRotation(this.cardRotateDeg,1000);
    //     },
    //     cardsScrollingRotateEffect(){
    //         // When scroll to Skill set page, trigger cardsRotation()
    //         const page = document.querySelector('#skill-set-page');
    //         const travelDistance = window.innerHeight + window.pageYOffset;
    //         const triggerPoint = page.offsetTop + page.offsetHeight/2;
    //         if (travelDistance > triggerPoint){
    //             this.cardsRotation(this.cardRotateDeg,500);
    //             //set capability value (the bar) of each technique
    //             this.SetCapabilityValue();
    //         } else {
    //             // this.cardsRotation();
    //         }
    //     },
    //     cardsRotation(deg=0,delayTime=0){
    //         // funtion that rotates the card.
    //         document.querySelectorAll('.card').forEach(card => {
    //             setTimeout(()=>{
    //                 card.style.transform = `rotateY(${deg}deg)`;
    //             },delayTime);
    //         })
    //     },
    //     SetCapabilityValue(){
    //         const v = {
    //             '#html-bar' : '100%',
    //             '#css-bar' : '100%',
    //             '#javascript-bar':'100%',
    //             '#vuejs-bar':'100%',
    //             '#reactjs-bar':'100%',
    //             '#nextjs-bar':'50%',
    //             '#reactNative-bar':'30%',

    //             '#python-bar':'100%',
    //             '#django-bar':'100%',
    //             '#nodejs-bar':'80%',
    //             '#expressjs-bar':'90%',
    //             '#php-bar':'60%',
    //             // '#laravel-bar':'20%',

    //             '#mysql-bar':'60%',
    //             '#mongodb-bar':'60%',
    //             '#postgresql-bar':'80%',

    //             '#solidity-bar':'40%',
    //             '#docker-bar':'80%',
    //             '#github-bar':'100%',
    //             '#indesign-bar':'100%',
    //             '#xd-bar':'90%',
    //             '#illustrator-bar':'70%',
    //             '#photoshop-bar':'70%'
    //         }

    //         Object.entries(v).forEach(([id, value])=>{
    //             document.querySelector(id).style.width = value;
    //         })
    //     } 
        
    // }
}
</script>

<style lang="scss" scoped>

.card-wrapper {

    position: relative;
    height:100%;
    width:100%;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    perspective: 100rem;
    background-color: rgba(223, 223, 223, 0.212);
   
    .card{
        position:absolute;
        width: 300px;
        height: 500px;
        border: thin solid rgba(238, 235, 235, .5);
        border-radius: 1rem;
        box-shadow: -0.5rem 1.5rem 1.8rem #4442424f;
        transform: translateX(-50%) translateY(-50%);
        transform: rotateY(0);
        background-color: #ffffff;
        transform-origin: center;
        transition:transform .5s;
        overflow: hidden;
        display: flex;
        flex-direction: column;

    
        .card-title{
            @include column-horizontal-center(); 
            height:70px;
            padding: 10px 0;;
            margin:30px;
        }

        h3{
            width:100%;
            margin:0;
            height:50%;
            font-size: 1.4rem;
            font-family: $quaternary-font;
            font-weight: 600;
            letter-spacing: 0.3rem;
            text-align: center;
            padding:0;
        }
        h4{
            margin-top:.1rem;
            width:100%;
            height:50%;
            font-size: 1.2rem;
            font-weight:100;
            letter-spacing: 0.3rem;
            color: $grey;
            text-align: center;
            padding:0;
        }
        

        .card-tech-chart{
            position: relative;
            display: flex;
            flex-direction: column;
            width:100%;
            height:calc(100% - 70px);
            overflow: hidden;
            gap:10px;
            padding: 0rem 20px 20px 10px;
        }
    }
}





</style>