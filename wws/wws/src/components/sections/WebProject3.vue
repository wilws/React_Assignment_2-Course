<template>
    <section class="web-project-3" id="web-project-3">

        <rotation-layout-3 ref="rotationLayoutRef3">
            
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
                <div class="slot-wrapper">
                    <div class="title-wrapper">
                        <div class="title">
                            <h1 v-html="mainTitle"></h1>
                            <h3>{{ subTitle }}</h3>
                        </div>
                    </div>
                    <div class="content-wrapper">
                        <div class="video-wrapper">
                            <video controls loop autoplay>
                                <source :src="require('@/assets/img/projects/web_project_3/optionkatze2.mp4')" type="video/mp4">
                            </video>
                        </div>
                        <div class="dialogue-wrapper">
                            <div class="dialogue1">
                                <p>Let start the app…</p>
                            </div>
                            <div class="dialogue2">
                                <p> We choose 0002.HK “CLP HOLDINGS” as testing company.</p>
                            </div>
                            <div class="dialogue3">
                                <p>We use 1 year  daily price record </p>
                            </div>
                            <div class="dialogue4">
                                <p>We test indicator “RSI”,
                                    <br>We buy when:
                                    <br> - RSI is lower than and equal to 20
                                    <br>
                                    <br>We sell when:
                                    <br> - RSI is higher than and equal to 70
                                </p>
                            </div>
                            <div class="dialogue5">
                                <p>For the long position, we close the position when:
                                    <br> - we have 10% profit or,
                                    <br> - We have 5% loss
                                    <br>For the short position, we close the position when:
                                    <br> - we have 20% profit or,
                                    <br> - We have 10% loss
                                    <br>
                                    <br>The holding period is “0” 
                                    <br>means no time restriction in holding.
                                </p>
                            </div>
                            <div class="dialogue6">
                                <p>Here is the result:
                                    <br>We traded 66 time.
                                    <br>
                                    <br>For long position:
                                    <br> - We have 16 trades
                                    <br> - in which 4  trades were loss, 
                                    <br> - 0 trade is win 
                                    <br> - other 12 trade is still on going 
                                    <br>   and not yet meet the close requirement
                                    <br>
                                    <br>For Short position:
                                    <br> - We have 25 trades
                                    <br> -  in which 0  trades were loss
                                    <br> - 21 trades were win
                                    <br> -  other 4 trade is still on going 
                                    <br>    and not yet meet the close’s requirement)
                                    <br>
                                    <br>The total profit is 265.65 HKD. 
                                </p>
                            </div>
                        </div>

                    </div>
                </div>
            </template>
            <!-- end of slot 2 -->

        </rotation-layout-3>
    </section>
</template>

<script>


import ProjectPageLayout from "../layout/ProjectPageLayout.vue";
import RotationLayout3 from "../layout/rotationLayout.vue";

export default {
    components:{
        ProjectPageLayout,
        RotationLayout3
    },
    mounted(){
        // pass proprs to "rotation-layout" slot
        this.$refs.rotationLayoutRef3.buttonSetting = { 
            backgroundColor : "#EAAB15",
            color:"White",
        }
        this.$refs.rotationLayoutRef3.boxClass = ".web-project-3 .space .box";
    },
    data(){
        return {
            // pass proprs to "project-page-layout" child component
            mainTitle : "Web Project 3",
            subTitle: "2019-OPTION KATZE II",
            linkToProjectDescription: "View Video Demo",
            projectIconUrl: require('@/assets/img/projects/web_project_3/logo.png'),
            FrontEndTechList: ['HTML/CSS','Javascript'],
            BackEndTechList: ['Python','Django', 'MySQL'],
            DesignStyleList: ['Ajax  for data exchange', 'Bootstrip for styling','JQuery'],
            mediaType:"image",
            mediaDisplayUrl: require('@/assets/img/projects/web_project_3/cover.png'),
            backgroundColor:"Black",
            fontColor:"white",
            id: "#web-project-3",
            buttonColor:"#EAAB15",
            projectDescription :

            "RSI, MACD, SMA…etc. Those mysterious words from Technical Analysis  (TA) are always seen in stock world. TA is a method to predict the price movement of an asset. But it is always blamed by fundamental investors that TA is nothing but astrology. So, to dig out how accurate TA could be in investment, I made this application for back testing difference TA strategies, to see wether it is really profitable if disciplinarily following the TA strategies.  Yahoo-finance API is used to extract historical price data."+
            "<br>"+
            "<br>"+
            "By clicking the  “View Video Demo” button above, you can see if I buy 0002.hk when RSI is lower than 20 and sell when hight than 70, it in the end is a profitable strategy.  But it doesn’t mean that we can have the same positive result if adopting the same strategy on other assets."
        }
    },
    methods:{
        workDisplay(){
            this.$refs.rotationLayoutRef3.rotate('forward');
        }
    }
}
</script>


<style lang="scss" scoped>
.web-project-3{
    width:100vw;
    height: 100vh;
    background-color: rgb(0, 0, 0);
}


.slot-wrapper{
    position: relative;
    width:100%;
    height:100%;
    padding: 4rem;
    background-color: black;
    color:white;
    @include column-horizontal-center();

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
        position:relative;
        width:100%;
        height: 80%;
        margin-top:5rem;
        text-align: left;
        display: flex;
        flex-wrap: wrap;
        // border:solid thin red;

        .dialogue-wrapper{
            position:relative;

            width:30%;
            height:100%;
        
            div{
                position:absolute;
                color:black;
                background-color: rgba(255, 255, 255, 0.678);
                font-size:2rem;
                text-align: left;
                z-index:2;
                padding:1rem 2rem;
                top: 0rem;
                border-radius: 5px;
            }

            .dialogue1{
                display: none;
                right:3rem;
                
            
            }
            .dialogue2{
                display: none;
                right:3rem;
    
            }
            .dialogue3{
                display: none;
                right:3rem;
            }
            .dialogue4{
                display: none;
                right:3rem;

            }
            .dialogue5{
                display: none;
                right:3rem;
            }
            .dialogue6{
                //  display: none;
                right:3rem;
            }
        }

        .video-wrapper{
            position:relative;
            width:70%;
            height:100%;
            background-color: transparent;
            z-index: 1;
            video{
                // height: 100%;
                width:100%;
                object-fit:cover;
            }
        }

    }
}

</style>