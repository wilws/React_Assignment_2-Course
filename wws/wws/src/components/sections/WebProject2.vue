<template>
    <section class="web-project-1">
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
    </section>
</template>

<script>

import ProjectPageLayout from "../layout/ProjectPageLayout.vue";

export default {
    components:{
        ProjectPageLayout
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
            window.open("https://ellowtradition-vue.herokuapp.com/", '_blank');
        }
    }
}
</script>


<style lang="scss" scoped>
.web-project-1{
    background-color: rgb(0, 0, 0);
}

</style>