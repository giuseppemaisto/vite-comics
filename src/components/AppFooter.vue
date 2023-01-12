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
        <div class="row">
            <div class="col">
                <ul>
                    <li><strong>DC COMICS</strong></li>
                    <li><a href="/">Characters</a></li>
                    <li><a href="/">Comics</a></li>
                    <li><a href="/">Movies</a></li>
                    <li><a href="/">TV</a></li>
                    <li><a href="/">Games</a></li>
                    <li><a href="/">Videos</a></li>
                    <li><a href="/">News</a></li>
                </ul>
                <ul>
                    <li><strong>SHOP</strong></li>
                    <li><a href="/">Shop DC</a></li>
                    <li><a href="/">Shop DC Collection</a></li>
                   
                </ul>
            </div>

            <div class="col">
                <ul>
                    <li><strong>DC</strong></li>
                    <li><a href="/">Term of Use </a></li>
                    <li><a href="/">Privacy policy (New)</a></li>
                    <li><a href="/">Add Choiches</a></li>
                    <li><a href="/">Advertising</a></li>
                    <li><a href="/">jobs</a></li>
                    <li><a href="/">Subscription</a></li>
                    <li><a href="/">Talent Workshop</a></li>
                    <li><a href="/">CPSC Certificates</a></li>
                    <li><a href="/">Ratings</a></li>
                    <li><a href="/">Shop Help</a></li>
                    <li><a href="/">Contact Us</a></li>
                </ul>
            </div>
            <div class="col">
                <ul>
                    <li><strong>SITES</strong></li>
                    <li><a href="/">DC</a></li>
                    <li><a href="/">MAD Magazine</a></li>
                    <li><a href="/">DC Kids</a></li>
                    <li><a href="/">DC Universe</a></li>
                    <li><a href="/">DC Power Visa</a></li>
                   
                </ul>
            </div>
        </div>
        <div class="logo-dc-footer">
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </div>
    <div class="socials-bar">

    </div>
</div>
</footer>
</template>
<style lang="scss">
     @use '../styles/partials/variable' as *;
    @use '../styles/partials/mixins' as *;
.footer-bar{
    background-color:#3880F1;
    
    .img-blue{
        width: 50px;
        padding: 5px;
        vertical-align: middle;
    }
}
.container{
        display: flex;
       padding: 40px;

       ul{
        list-style: none;
        
       display: flex;

        li a{
           
           
            padding: 40px;
            text-decoration: none;
            display: flex;
            align-items: center;
            color: white;
            padding: 0 30px;
            font-weight: 300;
           
            
        }
       }
}

.footer-faq{
    min-width: 1000px;
    height: 400px;
   display: flex;
    background-image: url(../assets/img/footer-bg.jpg);
   
    .logo-dc-footer{
      
        background-repeat: no-repeat;
        padding-left: 20%;
       
       
       
    
    }

    .row{
        display: flex;

        .col{
            padding: 50px;
    
            ul{
               
                list-style-type: none;
                padding-bottom: 10px;
        
                li{
                  @include text;
                }
                li a{
                  @include text-list;
                  font-size: 12px;
                }
            }
        }
    }
}
.socials-bar{
    width: 100%;
    height: 75px;
    background-color: black;
    position: absolute;
}

</style>