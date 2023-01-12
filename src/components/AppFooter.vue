<script>
export default {
    data(){
        return{
            menu:[
                {
                    img: 'buy-comics-digital-comics.png',
                    label: ' DIGITAL COMICS',
                    url:'#',
                    active: false,
                },
                {
                    img: 'buy-comics-merchandise.png',
                    label: ' DC MERCHANDISE',
                    url:'#',
                    active: true,
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    label: 'SUBSCRIPTION',
                    url:'#',
                    active: false,
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    label: 'COMIC SHOP LOCATOR',
                    url:'#',
                    active: false,
                },
                {
                    img: 'buy-comics-power-visa.png',
                    label: 'DC POWER VISA ',
                    url:'#',
                    active: false,
                },
            ]
        }
    },
    methods: {
        imgPath: function(img){
            return ` /src/assets/img/${img}`
        }
    },
}
</script>
<template lang="">
<footer>
    <div class="footer-bar">
    <div class="container">
        <ul>
                <li v-for="(item, index) in menu" ::key="index">
                <a :href="item.url" :class="item.active ? 'active': ''">
                <img :src="imgPath(item.img)" class="img-blue" alt=""> <div>{{item.label}}</div>
                </a>
                </li>
        </ul>
    </div>

    <div class="footer-faq">

    </div>
</div>
</footer>
</template>
<style lang="scss">
     @use '../styles/partials/variable' as *;
    @use '../styles/partials/mixins' as *;
.footer-bar{
    background-color: blue;
}
.img-blue{
    width: 50px;
    padding-right: 5px;
}
.container{
        display: flex;
       padding: 40px;

       ul{
        list-style: none;
        
       display: flex;

        li a{
            display: inline-block;
            padding: 40px;
            text-decoration: none;
            display: flex;
            color: white;
            font-size: 10px;
           
            
        }
       }
}

.footer-faq{
    max-width: 1000px;
    height: 400px;
    background-color: black;
    background-image: url(../assets/img/dc-logo-bg.png);
   background-repeat: repeat-x;
    
}

</style>