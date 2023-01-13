        <script>
        import ComicsData from "../assets/data/dc-comics.json"
        import ComicCard from './ComicCard.vue'
        export default {
            components:{
                ComicCard,
            },
            data() {
                return {
                    comics: ComicsData,
                }
            },
        }
        </script>
<template lang="">
    <div class="jumbotron">

    </div>
    <div class="dark">
        <div class="container">
            <div class="upper-title">
                <h2 class="title">
                    Comics Series 
                </h2>
            </div>
        </div>
        <div class="container">
            <div class="comics-container">
               <ComicCard v-for="(item, index) in comics" :key="index" :comic="item"/>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
     @use '../styles/partials/variable' as *;
    @use '../styles/partials/mixins' as *;


    .jumbotron{
        height: 400px;
        background-image: url('../assets/img/jumbotron.jpg');
    }
    .dark{
        background-color: rgb(24, 24, 24);


    }

    .upper-title{
        position: relative;
       


        .title{
            text-transform: uppercase;
            color: white;
            background-color: $primary;
        width:250px;
        padding: 10px;
        text-align: center;
        position: absolute;
        top:-25px;
        border: 1px solid black;
        }
    }

    .comics-container{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        padding-top: 5rem;
    }
</style>