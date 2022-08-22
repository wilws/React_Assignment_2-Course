<template>
    <a :href="id" @click="$emit('pageSelected')">
    <div class="menu-items">
        <h1 v-html="title"></h1>
        <h2 v-html="subTitle"></h2>
    </div>
    </a>


</template>

<script>
export default {
    props:[
        'title',
        'subTitle',
        'id'
    ]
}
</script>

<style lang="scss" scoped>
a {
     color: inherit;
    text-decoration: none;
}

.menu-items{
    
    text-align: right;
    font-family: 'Courier New';
    transition-duration: .5s; 
    &:hover{
        background-color: rgba(48, 47, 47, 0.377);
        color:rgb(80, 63, 63);
    }

    &:hover > h1,
    &:hover > h2 {
        border-right:4px solid #000000;
    }

    h1{
        width:100%;
        font-size: 2.9rem;
        letter-spacing: .7rem;
        font-weight: lighter;
        border-right: 4px solid #EBEBEB;

    }

    h2{
        width:100%;
        font-size: 2rem;
        letter-spacing: .7rem;
        padding-top:1rem;
        font-weight: bold;
        border-right: 4px solid #EBEBEB;
    }
}
</style>