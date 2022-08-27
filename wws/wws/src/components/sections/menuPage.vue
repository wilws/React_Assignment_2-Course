<template>
    <div class="menu-button"></div>

    <section class="menu close">
        <button @click="menuController" class="close-button">Close</button>
        <div class="menu-items-wrapper">
            <menu-item class="menu-item"
                v-for="(value,key) in items" 
                :key = "key" 
                :title =  "key"
                :subTitle = "value[0]" 
                :id = "value[1]" 
                @pageSelected = "menuController"
            ></menu-item>
             
        </div>

       

    </section>
</template>



<script>
import MenuItem from "../layout/menuItemLayout.vue";
export default {
    components:{
        MenuItem
    },
    data(){
        return{
            menuOpen:false,
            items : {
                "About": ["Who Am I","#index"],
                "Skill Set":["Skills That I Have","#skill-set-page"],
                "Web Project 1":["E-Commerce Website Using Vue.js + Node.js + Express.js","#web-project-1"],
                "Web Project 2":["Option Strategies Analysis Web Application Using Python + Django","#web-project-2"],
                "Web Project 3":["Back Testing Web Application Using Python + Django","#web-project-3"],
                "Web Project 4":["Simple HTML + CSS + JS Website","#web-project-4"],
                "Interior Design<br>Project":["Build Up a Studio","#interior-design-project-1"],
                "Graphic Design<br>Project":["Dessert Shop Re-Branding","#graphic-design-project-1"],
                "Course<br>Assignment":["Assignments done during<br>studying online course","#assignment"],
            }
        }
    },
    methods:{
        menuController(){
            document.querySelector(".menu").classList.toggle('close');
            document.querySelector(".menu-button").classList.toggle('close');
            this.menuOpen = !this.menuOpen;

            // lock the scroll bar
            if (this.menuOpen) {
                document.getElementsByTagName('body')[0].style.overflow = 'hidden';
            } else {
                document.getElementsByTagName('body')[0].style.overflow = 'visible';
            }
        }
    },
    mounted(){
        document.querySelector(".menu-button").addEventListener("mouseover",() => {
            this.menuController();
        });
    }
}
</script>

<style lang="scss">

// default size: iPhone 5 : 320px x 568px 


.menu-button{
    position:fixed;
    width:1.1rem;
    height:1.1rem;
    background-color: rgb(46, 46, 46);
    top:0.3rem;
    left:0.3em;
    z-index: 10;
}

.menu-button.close{
    opacity: 0;
    visibility:none;
    z-index: -1;
}


.menu.close{
    opacity: 0;
    visibility:none;
    z-index: -1;
}

.menu{
    position:fixed;
    z-index: 12;
    top:0;
    left:0;
    background-color: rgb(255, 255, 255);
    width:100%;
    height:100%;
    opacity: 1;
    visibility:unset;
    transition-property: opacity visibility;
    transition-duration: 1s;
    overflow: scroll;
    padding: 5px;
     padding-bottom: 10%;


    .close-button{
        position:fixed;
        left:0px;
        top:0px;
        font-family: 'Courier New';
        font-size: .9rem;
        letter-spacing: .15rem;
        // background-color: rgba(0, 0, 0, 0.267);
        padding: 1px;
        padding-left: 2.5px;
        border: none;
        cursor: pointer;
        z-index: 2;
    }

    .menu-items-wrapper{
        width:100%;
        padding-right:10px;
        padding-top:10px;
        display: flex;
        flex-direction: column;
        gap:50px;

        @media (min-width : 768px) and (min-height: 600px){
            position: absolute;
            width:100%;
            height:100%;
            // border:red thin solid;
            // top:50%;
            // left:-2%;
            // transform:translateY(-50%);
            // width:90%;
            padding: 2rem;
            // padding-left:4rem;
            display: grid;
            grid-template-columns: repeat(2,45%);
            grid-template-rows:  repeat(5);
            grid-row-gap:50px;
            grid-column-gap:50px;
            grid-template-areas:
            "a f"
            "b g"
            "c h"
            "d i"
            "e j";

            .menu-item{
                // border:red thin solid;
            }

            .menu-item:nth-child(1){
                grid-area: a;
            }
            .menu-item:nth-child(2){
                grid-area: b;
            }
            .menu-item:nth-child(3){
                grid-area: c;
            }
            .menu-item:nth-child(4){
                grid-area: d;
            }
            .menu-item:nth-child(5){
                grid-area: e;
            }
            .menu-item:nth-child(6){
                grid-area: f;
            }
            .menu-item:nth-child(7){
                grid-area: g;
            }

            .menu-item:nth-child(8){
                grid-area: h;
            }

            .menu-item:nth-child(9){
                grid-area: i;
            }
        
        }

        @media (min-width : 1024px) and (max-height: 1024px) and (min-height: 700px){

            position: absolute;
            width:100%;
            height:100%;
            padding: 0rem;
            padding-right:6rem;
            padding-top:2rem;
            display: grid;
            grid-template-columns: repeat(3,30%);
            grid-template-rows:  repeat(4);
            // grid-row-gap:2%;
            // grid-column-gap:%;
            grid-template-areas:
            "a e i"
            "b f j"
            "c g k"
            "d h l";

            .menu-item{
                // border:red thin solid;
            }

            .menu-item:nth-child(1){
                grid-area: a;
            }
            .menu-item:nth-child(2){
                grid-area: b;
            }
            .menu-item:nth-child(3){
                grid-area: e;
            }
            .menu-item:nth-child(4){
                grid-area: f;
            }
            .menu-item:nth-child(5){
                grid-area: g;
            }
            .menu-item:nth-child(6){
                grid-area: h;
            }
            .menu-item:nth-child(7){
                grid-area: i;
            }

            .menu-item:nth-child(8){
                grid-area: j;
            }

            .menu-item:nth-child(9){
                grid-area: k;
            }
        
        }

        @media (min-width : 1366px) and (min-height: 1024px){

            position: absolute;
            width:100%;
            height:100%;
            padding: 3rem;
            padding-right:6rem;
            padding-top:5rem;
            display: grid;
            grid-template-columns: repeat(3,30%);
            grid-template-rows:  repeat(4);
            // grid-row-gap:2%;
            // grid-column-gap:%;
            grid-template-areas:
            "a e i"
            "b f j"
            "c g k"
            "d h l";
        }
        

    }


    
}


</style>