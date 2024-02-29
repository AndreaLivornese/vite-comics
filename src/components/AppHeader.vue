<script>

export default{
  name:"AppHeader",

  data(){
    return{
        navLinks : [
            "Characters","Comics", "movies", "tv", "Games", "Collectibles", "videos", "Fans", "news", "Shop" 
        ],

    }
  },
}
</script>

<template>
 
 <div class="container">
     <nav>
         <div>
             <img src="/img/dc-logo.png" alt="">
         </div>
         <div>
             <ul class="links">
                 <li v-for="currentLink in navLinks">
                     <a href="">{{currentLink}}</a>
                 </li>
             </ul>
         </div>
 
     </nav>
 </div>

</template>

<style lang="scss">
@use '../style/mixins' as *;

.container{
    @include container;
}

nav{
    display:flex;
    justify-content: space-between;
    align-items: center;

    padding: 20px 0;
}

.links{
    display:flex;
    padding: 0;
    list-style-type:none;
    
    li{
        padding:12px 16px; 

        a{
            text-decoration: none;
            color:#4b535a;
        }
    }

}



</style>
