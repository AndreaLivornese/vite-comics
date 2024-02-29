<script>

export default{
  name:"AppFooter",

  data(){
    return{
       
        footerLinks:[
            {
                title:"DC COMICS",
                links:[
                    "Characters",
                    "Comics",
                    "Movies",
                    "TV",
                    "Games",
                    "Videos",
                    "News"
                ] ,
            },
            {
                title:" DC",
                links:[
                    "Terms Of Use",
                    "Privacy policy (New)",
                    "Ad Choices",
                    "Advertising",
                    "Jobs",
                    "Subscriptions",
                    "Talent Wprkshops",
                    "CPSC Certificates",
                    "Ratings",
                    "Shop Help",
                    "Contact Us",
                ] ,
            },
            {
                title:"SITES",
                links:[
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Visa",
                ] ,
            },
            {
                title:"SHOP",
                links:[
                    "Shop DC",
                    "Shop DC Collectibles"
                ] ,
            },
            
        ],

        icons:[
            "/img/footer-facebook.png",
            "/img/footer-periscope.png",
            "/img/footer-pinterest.png",
            "/img/footer-twitter.png",
            "/img/footer-youtube.png",
        ],

    }
  },
}
</script>

<template>
 
<footer>

    <div class="container">

        <div class="footer-top">
            <div class="footer-links">
    
                <ul v-for="currentColumn in footerLinks">
                    <h3>{{ currentColumn.title }}</h3>
    
                    <li v-for="currentLink in currentColumn.links">
                        <a href="#">{{ currentLink }}</a>
                    </li>
                </ul>
    
            </div>
    
            <img src="/img/dc-logo-bg.png" alt="">

        </div>

        
        
    </div>

    <div class="footer-bottom">

        <div class="container">

            <div class="inner-footer-bottom">
                <div><a class="btn" href="#">SING-UP NOW!</a></div>
        
                <div class="social">
                    <div class="footer-text">
                        FOLLOW US
                    </div>
                    <div class="footer-icons">
                        <img v-for="currentIcon in icons" :src="currentIcon" alt="icona social">
                    </div>
                </div>
            </div>

        </div>

    </div>

</footer>

</template>

<style lang="scss">
@use '../style/mixins' as *;
@use '../style/_variables' as *;


footer{
    background-image:url("/img/footer-bg.jpg");;
    background-size: cover;
    
    overflow: hidden;


    .container{
        padding: 40px 0 50px;
    }
    
    .footer-top{
        position: relative;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;



        img{
            position:absolute;
            right:60px;
            top:-80px;

            transform: scale(120%);
        }
    }
}

.footer-links{
    display:flex;
    flex-flow: row wrap;
    align-items: flex-start;

    column-gap:50px;

    max-width: 400px;


    ul{
        list-style-type: none;
        padding: 0;

    }

    h3{
        font-size: 18px;
    }

    a{
        text-decoration: none;
        font-size:12px;
        color: rgba(255, 255, 255, .3);
    }
}


.footer-bottom{
    position: relative;
    z-index:1;
    
    
    background-color: #303030;

    .container{
        padding:30px 0;
    }


    .inner-footer-bottom{
        display: flex;
        justify-content: space-between;
        align-items: center;

        
        .btn{
            display: inline-block;
    
            padding:15px;
    
            border:2px solid $primaryColor;
    
            text-decoration: none;
            font-size:14px;
            font-weight: bold;
            color:white;
        }


        .social{
            display: flex;
            align-items: center;
            gap:25px;


            .footer-text{
                color:$primaryColor;
            }

            .footer-icons{
                display:flex;
                gap:10px;

                &>img{
                    cursor:pointer;
                }
            }
        }

    }


}



</style>
