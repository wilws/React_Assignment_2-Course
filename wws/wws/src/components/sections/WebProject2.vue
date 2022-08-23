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
                @work-display = "workDisplay"
            ></project-page-layout>
        </template>
        <!-- end of slot 1 -->

        <!-- slot 2-->
        <template v-slot:slot2>
            <div class="slot-wrapper">
                <img :src="require('@/assets/img/projects/web_project_2/logo.png')" class="background-logo" />
                <div class="title-wrapper">
                    <div class="title">
                        <h1 v-html="mainTitle"></h1>
                        <h3>{{ subTitle }}</h3>
                    </div>
                </div>
                <div class="content-wrapper">
                    <div class="upper">
                        <p>It is out of my expectation that Option Katze can dig out arbitrage chance. In the red circle, it shows that  if we make a “Long Butterfly” combination, the cost to pay is -7.32 HKD and the premium to receive is 7.38HKD. The difference of 0.06HKD means no matter where the price goes (up or down), that 0.06HKD is for sure in your wallet. If you are so lucky that the price eventually falls on the desired point, you can take 2.56HKD.</p>
                        <div class="img">
                            <img :src="require('@/assets/img/projects/web_project_2/PHOTO-2020-10-26-02-22-18.jpg')" alt="">
                        </div>
                    </div>
                    
                     <div class="lower">
                        <div class="img">
                            <img :src="require('@/assets/img/projects/web_project_2/PHOTO-2020-10-26-02-29-56.jpg')" alt="">
                        </div>
                        <div class="img">
                            <img :src="require('@/assets/img/projects/web_project_2/PHOTO-2020-10-25-13-44-32.jpg')" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </template>
        <!-- end of slot 2 -->

        <!-- slot 3-->
        <template v-slot:slot3>
            <div class="slot-wrapper">
                <img :src="require('@/assets/img/projects/web_project_2/logo.png')" class="background-logo" />
                <div class="title-wrapper">
                    <div class="title">
                        <h1 v-html="mainTitle"></h1>
                        <h3>{{ subTitle }}</h3>
                    </div>
                </div>
                <div class="content-wrapper">
                    <div class="upper">
                        <p>Later I deployed the application on Google AppEngine. But it costed a lot and I finally gave up.</p>
                        <div class="img">
                            <img :src="require('@/assets/img/projects/web_project_2/appEngiene.png')" alt="">
                        </div>
                    </div>
                    
                     <div class="lower">
                        <p>I also embeded ads inside the application. Finally I just can earn 148.17 HKD. Though the amount is so poor, but it is such a great experience to integrate application to Google’s services.</p>
                        <div class="img">
                            <img :src="require('@/assets/img/projects/web_project_2/AdSense.png')" alt="">
                        </div>
                    </div>
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
            projectDescription :"Several years ago I was so fascinated in option trading after reading Sheldon Natenberg’s  “Option Volatility & Pricing: Advanced Trading Strategies and Techniques”. It is fun to know that there are so many contract combinations to adopt. One day, I was tired to calculate the profit and return of each combination manually. I wished there was a application that can automatically scrape market data from finance website, calculate option price and volatility, test all the possible combination and finally tell you which is worth to trade. <br><br> After having such idea I instantly enrolled in a Python and Django course in Udemy and spend quite a lot of time to learn how to use the Django framework and other useful package like NumPy, Pandas, etc. <br><br>After building all the functions I want. I have an amazing discovery - Arbitrage . One night I ran the application and looped through all the option combinations, I found that there was a strategy that cost zero or even negative cost! It means that you constructed a combination in which the amount of premium received from short position is more than amount of cost you pay for the long position. Though it was an astonishing discovery,  chance like this, to be honest is so rare. <br><br>I later hosted the application on Google AppEngine and also joined Google AdSense, wishing to earn some to cover the expensive hosting cost. However it was not successful.  As the cost of hosting was so high and my day work did not allows me to so fascinate in trading anymore, there is no more maintenance on the application. The app is depreciated and not able to function now."
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
.web-project-1{
    background-color: rgb(0, 0, 0);
}

.slot-wrapper{
    position: relative;
    width:100%;
    height:100%;
    padding: 4rem;
    background-color: black;
    color: white;
    @include column-horizontal-center();

    .background-logo{
        opacity: 0.2;
         @include vertical-center();
        z-index: 0;
    }

    .title-wrapper{
        
        width:100%;

        .title{
            h1{
                width:100%;
                font-family: $secondary-font;
                font-size:4rem;
                letter-spacing: .1rem;
                text-align: left;
            }
            h3{
                    width:100%;
                    font-size: 2.1rem;
                    font-weight: 500;
                    font-family: $secondary-font;
                    letter-spacing: .2rem;
                    padding-left:.4rem;
                    margin-top:-.5rem;
                    text-align: left;
            }
        }
    }

    .content-wrapper{
        width:100%;
        height: 85%;
        margin-top:5rem;
        text-align: center;

        .upper{
            width:100%;
            height:50%;
            // border:solid red thin;
            display:flex;

            p{
                width:50%;
                // border:solid green thin;
                font-family: $primary-font;
                font-size: 2.3rem;
                text-align: left;
            }

            .img{
                width:50%;
                height:100%;
                //  border:solid purple thin;
                z-index:1;
                 padding: 1rem;
                 img{
                     height:100%;
                     width:100%;
                     object-fit: contain;
                     

                 }
            }
        }

        .lower{
            width:100%;
            height:50%;
            display:flex;
            // border:solid rgb(13, 15, 185) thin;

            p{
                width:50%;
                // border:solid green thin;
                font-family: $primary-font;
                font-size: 2.3rem;
                text-align: left;
            }
                        

            .img{
                width:50%;
                height:100%;
                // border:solid purple thin;
                padding: 1rem;
                z-index:1;
                img{
                     height:100%;
                     width:100%;
                     object-fit: contain;

                }
            }
        }


    }
}

</style>