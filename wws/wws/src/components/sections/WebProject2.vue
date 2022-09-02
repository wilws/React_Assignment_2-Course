<template>
    <section class="web-project-2" id="web-project-2">

        <rotation-layout-2 ref="rotationLayoutRef2">

        <!-- slot 1-->    
        <template v-slot:slot1>
            <project-page-layout
                :mainTitle = "mainTitle"
                :subTitle = "subTitle"
                :linkToProjectDescription = "linkToProjectDescription"
                :projectIconUrl = "projectIconUrl"
                :projectDescription = "projectDescription"
                :FrontEndTechList = "FrontEndTechList"
                :BackEndTechList = "BackEndTechList"
                :DesignStyleList = "DesignStyleList"
                :mediaDisplayUrl = "mediaDisplayUrl"
                :mediaType = "mediaType"
                :backgroundColor = "backgroundColor"
                :fontColor = "fontColor"
                :buttonColor = "buttonColor"
                :id = "id"
                @work-display = "workDisplay"
            ></project-page-layout>
        </template>
        <!-- end of slot 1 -->

        <!-- slot 2-->
        <template v-slot:slot2>
            <div class="slot2-wrapper">
                <img :src="require('@/assets/img/projects/web_project_2/logo.png')" class="background-logo" />
                <div class="title-wrapper">
                    <div class="title">
                        <h1 v-html="mainTitle"></h1>
                        <h3>{{ subTitle }}</h3>
                    </div>
                </div>

                <div class="content-wrapper">
                    <div class="flex-box description-wrapper">
                        <div>
                            <h6>Dig out Arbitrage Chance </h6>
                            <p>
                                <br>
                                <br>
                                In the red circle of the Picture-1, it shows that  if we make a “Long Butterfly” combination, the cost to pay is -7.32 HKD and the premium to receive is 7.38 HKD. The difference of 0.06 HKD means no matter where the price goes (up or down), that 0.06 HKD is for sure in your wallet. If you are so lucky that the price eventually falls on the desired point, you can take 2.56 HKD. 
                            </p>
                        </div>
                    </div>
                    <div class="flex-box img">
                        <img :src="require('@/assets/img/projects/web_project_2/PHOTO-2020-10-26-02-22-18.jpg')" alt="">
                        <p>Picture-1</p>
                    </div>
                     <div class="flex-box img">
                            <img :src="require('@/assets/img/projects/web_project_2/PHOTO-2020-10-26-02-29-56.jpg')" alt="">
                            <p>Picture-2</p>
                    </div>
                     <div class="flex-box img">
                            <img :src="require('@/assets/img/projects/web_project_2/PHOTO-2020-10-25-13-44-32.jpg')" alt="">
                            <p>Picture-3</p>
                    </div>
                </div>
            </div>
        </template>
        <!-- end of slot 2 -->

        <!-- slot 3-->
        <template v-slot:slot3>
            <div class="slot2-wrapper">
                <img :src="require('@/assets/img/projects/web_project_2/logo.png')" class="background-logo" />
                <div class="title-wrapper">
                    <div class="title">
                        <h1 v-html="mainTitle"></h1>
                        <h3>{{ subTitle }}</h3>
                    </div>
                </div>


                <div class="content-wrapper">
                    <!-- <div class="flex-box description-wrapper slot3">
                        <div>
                        <h6>Deploy on Google Cloud</h6>
                        <p>
                            <br>
                            <br>
                            Later I deployed the application on Google AppEngine. But it costed a lot and I finally gave up.
                        </p>
                        </div>
                    </div>
                    <div class="flex-box img slot3">
                        <img :src="require('@/assets/img/projects/web_project_2/appEngiene.png')" alt="">
                    </div>
                    <div class="flex-box description-wrapper slot3 ">
                        <div>
                        <h6>Google AdSense</h6>
                        <p>
                            <br>
                            <br>
                            I also embeded ads inside the application. As lacking of advertisement of the website, it just could earn 148.17 HKD. Though the amount is so poor, but it is such a great experience to integrate application to Google’s services.
                        </p>
                        </div>
                    </div> -->
                     <!-- <div class="flex-box img slot3">
                            <img :src="require('@/assets/img/projects/web_project_2/AdSense.png')" alt="">
                    </div> -->
                </div>
            </div> 
        </template>
        <!-- end of slot 3 -->


        </rotation-layout-2>

    </section>
</template>

<script>

import ProjectPageLayout from "../layout/ProjectPageLayout.vue";
import RotationLayout2 from "../layout/rotationLayout.vue";


export default {
    components:{
        ProjectPageLayout,
        RotationLayout2
    },

    mounted(){
        // pass proprs to "rotation-layout" slot
        this.$refs.rotationLayoutRef2.buttonSetting = { 
            backgroundColor : "#0099AF",
            color:"White",
        }

        this.$refs.rotationLayoutRef2.boxClass = ".web-project-2 .space .box";

        
    },
    data(){
        return {
            mainTitle : "Web Project 2",
            subTitle: "2018-OPTION KATZE",
            linkToProjectDescription: "View Project Description",
            projectIconUrl: require('@/assets/img/projects/web_project_2/logo.png'),
            FrontEndTechList: ['HTML/CSS','Javascript'],
            BackEndTechList: ['Python','Django', 'MySQL'],
            DesignStyleList: ['Ajax  for data exchange', 'Bootstrip for styling','JQuery', 'Beautifulsoup for web scrapping'],
            mediaType:"image",
            mediaDisplayUrl: require('@/assets/img/projects/web_project_2/cover.png'),
            backgroundColor:"Black",
            fontColor:"white",
            buttonColor:"#0099AF",
            id: "#web-project-2",
            projectDescription :
            "I was so fascinated in option trading after reading Sheldon Natenberg’s  “Option Volatility & Pricing: Advanced Trading Strategies and Techniques”. The charm of option is that you can adopt numerous strategies by combining selling or buying action of put and call contract."+
            "<br>"+
            "<br>One day, I was tired to calculate the profit and return of each strategy manually. I wished there was an application that could automatically scrape market data from internet, calculate contract price and volatility, test all the possible combinations and finally tell you which is worth to trade."+
            "Therefore I created one with Python and Django. The reason to choose python as the major tool is due to its useful package like NumPy and Pandas which facilitates in scientific calculation."+
            "<br>"+           
            "<br>When all the functions I want were created. I have an amazing discovery - Arbitrage. Please click the \"View Project Description\" button above to see the detail."+
            "<br>"+
            "<br>I later hosted the application on Google AppEngine and also joined Google AdSense, wishing to earn some to cover the expensive hosting cost. However it was not successful."+          
            "As I seldom trade option later and the cost of hosting was so high, there is no more maintenance on the application. Some packages in the app are depreciated. Though Option Katze is not be able to function now, it is a valuable experience to utilise programming knowledge to tackle problem in other sector."
        }
    },
    methods:{
        workDisplay(){
            this.$refs.rotationLayoutRef2.rotate('forward');
        }
    }
}
</script>


<style lang="scss" scoped>
.web-project-2{
    background-color: rgb(0, 0, 0);
}

.slot2-wrapper{
    position: relative;
    width:100%;
    height:100%;
    padding: 1rem;
    background-color: black;
    color: white;
    @include column-horizontal-center();
    // border:red solid thin;

    .background-logo{
        @include vertical-center();
        opacity: 0.2;
        width:50%;
        height:50%;
        object-fit: contain;
        z-index: 0;
    }

    .title-wrapper{
        position:relative;
        width:100%;

        .title{
            position: relative;
            width:100%;
            min-height:44px;
            min-width:284px;
            display: flex;
            flex-direction: column;
            justify-content: start;
            // border:red thin solid;
        
            h1{
                position: relative;
                width:100%;
                font-family: $secondary-font;
                font-size:1.1rem;
                letter-spacing: 0rem;
                text-align: left; 
            }

            h3{
                position: relative;
                width:100%;
                font-size: 0.6rem;
                font-weight: 500;
                font-family: $secondary-font;
                letter-spacing: .1rem;
                padding-left: .2rem;
                text-align: left;
            }
        }
    }

    .content-wrapper{
        display: flex;
        flex-direction: column;    
        width:100%;
        margin-top:2rem;
        column-gap: 2px;
        row-gap: 10px;
        overflow: scroll;
        

        @media(min-width:1024px) and (max-height:1024px){
            flex-direction: unset; 
            flex-wrap: wrap;   
            justify-content: space-between;
            padding:0 2rem;
        }

        .flex-box{
            width:100%;
            // border:thin solid red;

        }

        .description-wrapper{
            position: relative;
            width:100%;

  

            div{
                width:100%;
                text-align: center;
                display: flex;
                justify-content: start;
                flex-direction: column;
                margin-top:2rem;
                // border:thick rgba(255, 255, 255, 0.74) solid;
                h6{
                    width:100%;
                    font-size:1.5rem;
                    margin:0;
                }

                p{
                    width:100%;
                    font-family: $primary-font;
                    color:white;
                    font-size: .8rem;
                    letter-spacing: .1rem ;
                    line-height: 1.5rem;
                    padding:0;
                    margin-top:-2rem;

                }
            }
        }


        .img{
            position: relative;
            height:50%;
            min-height:170px;
            z-index:1;
            width:100%;
            @media(min-width:1024px) and (max-height:1024px){
                width:30%;
            }

            &.slot3{
                @media(min-width:1024px) and (max-height:1024px){
                    width:100%;
                    text-align: center;
                }
                img{
                    @media(min-width:1024px) and (max-height:1024px){
                        width:30%;
                    }
                }
            }
            img{
                z-index:1;
                width:100%;
                height:100%;
                
                border:thick rgba(255, 255, 255, 0.74) solid;
                object-fit: cover;
            }

            p{
                position: absolute;
                z-index: 2;
                bottom: .5rem;
                left: .5rem;
                // width: 100%;
                height: 1.5rem;
                line-height: 2.2rem;
                // text-align: left;
                color: white;
                font-size: 0.9rem;
                // margin-left: 1rem;
                padding: 0 1rem;
                letter-spacing: 0.2rem;
                font-family: sans-serif;
                font-weight: 100;
                background-color: rgba(0, 0, 0, 0.336);
            }
        }

        .img:nth-child(3){
            // text-align: right;
        }

    }
}

</style>