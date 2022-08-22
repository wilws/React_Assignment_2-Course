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
                "Web Project 1":["E-Commerce Website Using<br>Vue.js + Node.js +<br>Express.js","#web-project-1"],
                "Web Project 2":["Option Strategies Analysis<br>Web Application Using<br>Python + Django","#web-project-2"],
                "Web Project 3":["Back Testing Web<br>Application Using<br>Python + Django","#web-project-3"],
                "Web Project 4":["Simple HTML + CSS + JS<br>Website","#web-project-4"],
                "Interior Design<br>Project":["Build Up a Studio","#interior-design-project-1"],
                "Graphic Design<br>Project":["Dessert Shop Re-Branding","#graphic-design-project-1"],
                "Course<br>Assignment":["Assignments done during studying online course","#assignment"],
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

.menu-button{
    position:fixed;
    width:2rem;
    height:2rem;
    background-color: rgb(46, 46, 46);
    top:1rem;
    left:1rem;
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
    padding: 5rem;
    opacity: 1;
    visibility:unset;
    transition-property: opacity visibility;
    transition-duration: 1s;


    .close-button{
        font-family: 'Courier New';
        font-size: 2rem;
        letter-spacing: .4rem;
        background-color: white;
        border: none;
        cursor: pointer;
        position:absolute;
        width:1rem;
        height:1rem;
    }

    .menu-items-wrapper{
        // border:thin red solid;
        position: absolute;
                top:50%;
                left:-2%;
        transform:translateY(-50%);
        width:90%;
        padding: 5rem;
        display: grid;
        grid-template-columns: repeat(3,30%);
        grid-template-rows:  repeat(4);
        grid-row-gap:8rem;
        grid-column-gap:8rem;
        grid-template-areas:
        "a e i"
        "b f j"
        "c g k"
        "d h l";

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

    
}


</style>