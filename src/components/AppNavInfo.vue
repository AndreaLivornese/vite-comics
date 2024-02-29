<script>

export default{
  name:"AppNavInfo",

  data(){
    return{
       
        informations:[
            {
                img:'/img/buy-comics-digital-comics.png',
                txt: 'DIGITAL COMICS',
            },
            {
                img:'/img/buy-comics-merchandise.png',
                txt: 'DC MERCHANDISE',
            },
            {
                img:'/img/buy-comics-subscriptions.png',
                txt: 'SUBSCRIPTION',
            },
            {
                img:'/img/buy-comics-shop-locator.png',
                txt: 'COMIC SHOP LOCATOR',
            },
            {
                img:'/img/buy-dc-power-visa.svg',
                txt: 'CD POWER VISA',
            },
        ],

    }
  },
}
</script>

<template>
 
<section class="sec-info">

    <div class="container">
    
        <ul class="info">
            <li v-for="currentInfo in informations" class="info-link">
                <div class="img-box">
                    <img :src="currentInfo.img" alt="immagini">
                </div>
                <div class="info-txt">
                    <a href="#">{{ currentInfo.txt }}</a>
                </div>
            </li>
        </ul>

    </div>

</section>

</template>

<style lang="scss">
@use '../style/mixins' as *;
@use '../style/_variables' as *;


.sec-info{
    padding:50px 0;
    background-color: $primaryColor;


    .info{
        display: flex;
        justify-content: center;
        gap:70px;

        list-style-type: none;
        padding: 0;


        .info-link{
            display: flex;
            align-items: center;
            gap:10px;


            .img-box{
                height: 55px;


                img{
                    height: 100%;
                }
            }

            a{
                text-decoration: none;
                color:white;
                font-size:14px;
            }
        }
    }
}




</style>
