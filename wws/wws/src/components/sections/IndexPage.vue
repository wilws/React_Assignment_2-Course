<template>
    <section class="index-page" id="index">
        <div class="name">
            <h1>WAISHUN</h1>
            <h1>WONG</h1>
        </div>

        <div class="introduction-wrapper">
            <div class="introduction">
                I am Wai Shun WONG, a self-taught full stack web developer. 
                <br>I specialise in VueJs, HTML and CSS/SACS/SCSS to construct frontend web application. For the backend side, I am proficient in using Python + Django or NodeJs + Express framework. I can construct RESTful API for the communication of both front and back ends. I also have knowledge to connect application to MySQL / MongoDB  to preform CRUD.
                <br>“Learn” and “Create” are what I passionate about. From design to coding and even to investment, applying newly absorbed knowledge to solve the problem encountered in reality brings me a great satisfaction. 
                <br>After Obtaining a Bachelor Degree in Biology in Hong Kong, I pursued a Postgraduate Diploma in Investment Management and Financial Intelligence. The knowledge obtained from postgraduate diploma always stimulating me what programming can do in financial aspect.  I recently finished a course of Solidity and Ethereum. I am seeking chances to participate in a relative project. But, I will never confine myself in single area as life is a journey of learning. My passion for learning and coding drive me to try and challenge as much as I can, no matter it is a frontend project, backend project or others.
          </div>
        </div>

        <div class="img-wrapper">
            <img :src="require('@/assets/img/font_page/portfile.jpg')">
        </div>

        <div class="contact">
            <p>github : https://github.com/wilws</p>
            <p>email : wilson.ws.pro@gmail.com</p>
        </div>
    </section>
</template>

<script>
export default {
    setup() {
        
    },
}
</script>

<style lang="scss" scoped>

.index-page{
    width:100%;
    height:100%;
    display: flex;
    background-color: white;
    overflow: hidden;
    // border-bottom:grey thin solisrd;
    
}

.index-page{

    .name{
        position:absolute;
        font-family: 'Noto Sans TC', sans-serif;
        font-size: 6rem;
        letter-spacing: 1.3rem;
        text-align: right;
        left:26%;
        z-index: 1;
        background-color: rgba(256,256,256,0.5);
    

        h1:nth-child(2){
            margin-top:-4rem;
        }

    }

    .introduction-wrapper{
        display: flex;
        @include vertical-horizontal-center();
        width:55%;
        z-index: 2;
   

        .introduction{
            margin-top:25rem;
            width:65%;
            height:100%;
            font-family: $primary-font;
            color:$grey ;
            font-size: 1.3rem;
            letter-spacing: .1rem ;
            line-height: 3rem;
            text-align: justify;
            padding-bottom: 0;

            p{
                margin-top:4rem;
                padding-bottom: 0;
            }
        }


    }

    .img-wrapper{
        position: relative;
        width:45%;
        background-color: red;
        overflow: hidden;

        img{
            height: 100%;
            width:100%;
            object-fit: cover;
        }
    }

    .contact{
        position:absolute;
        right:5rem;
        bottom:5rem;
        color: rgb(141, 139, 139);
        font-family: $secondary-font;
        font-size: 1.4rem;
        letter-spacing: 0.3rem;
        text-align: right;

    }
}


</style>