        <script>
        export default {
            props:{
                comic: Object
            }
        }
        </script>
<template lang="">
    <div>
        <div class="comic-card">
            <div class="thumb-container">
                <img :src="comic.thumb" class="thumb" :alt="comic.series">
            </div>
            <div class="title-container">
                <h4>{{comic.series}}</h4>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
     @use '../styles/partials/variable' as *;
    @use '../styles/partials/mixins' as *;

    .comics-card{
        margin:10px;
        width: calc(100% / 6 - 40px);
        margin-bottom : 50px;

        .thumb-container{
            width: 100%;

        }

        .title-container{
            text-align: center;
            color: white;
            padding: 10px;
        }
    }
</style>