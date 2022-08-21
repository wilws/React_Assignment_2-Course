<template>
    <section class="index-page">
        <div class="name">
            <h1>WAISHUN</h1>
            <h1>WONG</h1>
        </div>

        <div class="introduction-wrapper">
            <div class="introduction">
                <p>My name is Wai Shun WONG. I am a self-taught full stack web developer. I specialise in VueJs, HTML/CSS for front end construction.  For the backend, I use Python with Django, NodeJs with Express. I can connect application to mySQL / Mongo database to preform CRUD. I can construct RESTful API for the communication of front and back ends.</p>
                <p>I love learning. Applying newly absorbed knowledge to solve the problem encountered in reality brings me a great satisfaction. Moreover, the passion of programming drives me to explore more and more.  I recently finished an online course of Solidity and Ethereum. I am seeking chances to make a blockchain project.</p>
                <p>After Obtaining a Bachelor Degree in Biology in Hong Kong, I pursued a Postgraduate Diploma in Investment Management and Financial Intelligence. The knowledge obtained from postgraduate diploma always stimulating me what programming can do in financial world.</p>
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
    
}

.index-page{

    .name{
        position:absolute;
        font-family: 'Noto Sans TC', sans-serif;
        font-size: 8rem;
        letter-spacing: 1.3rem;
        text-align: right;
        left:32.4%;
        z-index: 10;
        background-color: rgba(256,256,256,0.5);
    
        // h1:nth-child(1){
      
        // }

        h1:nth-child(2){
            margin-top:-6rem;
        }

    }

    .introduction-wrapper{
        display: flex;
        @include vertical-horizontal-center();
        width:55%;
   

        .introduction{
            margin-top:40rem;
            width:60%;
            height:100%;
            font-family: $primary-font;
            color:$grey ;
            font-size: 2rem;
            letter-spacing: .1rem ;
            line-height: 4rem;
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