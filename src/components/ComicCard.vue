        <script>
        export default {
            props:{
                comic: Object
            }
        }
        </script>
<template lang="">
    
        <div class="comic-card">
            <div class="thumb-container">
                <img :src="comic.thumb" class="thumb" :alt="comic.series">
            </div>
            <div class="title-container">
                <h4>{{comic.series}}</h4>
            </div>
      </div>
    
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variable' as *;
    

    .comics-card{
       margin: 10px;
        width: calc(100% / 6 - 20px );
        margin-bottom : 50px;
     

        
        .thumb-container{
            width: 100%;
            height: 200px;
    
            .thumb{
                height: 100%;
                width: 100%;
                object-fit: cover;
                object-position: top;
                
            }
        }
            
        
        .title-container{
            object-position: top;
            object-fit: cover;
            text-align: center;
            color: white;
            padding: 5px;
            text-transform: uppercase;
        }
     }
</style>