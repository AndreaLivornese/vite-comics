<script>

export default{
  name:"AppComicsItem",

  props: {

    imgCardUrl: String,
    comicsTitle: String,
  },

  data(){
    return{
       
        
    }
  },
}
</script>

<template>
 
    <div class="card">
        <div class="card-img">
            <img :src="imgCardUrl" alt="immagine del fumetto">
        </div>
        <div class="comics-title">
            {{ comicsTitle }}
        </div>
    </div>

</template>

<style lang="scss">
@use '../style/mixins' as *;


.card{
    width: calc(185px);


    .card-img{
        max-width: 185px;
        height: 185px;
        margin-bottom: 20px;
        overflow: hidden;

        img{
            width:100%;
        }
    }

    .comics-title{
        text-align: center;
        font-size:14px;
        text-transform: uppercase;
        color:white;
        font-weight: bold;
    }
}

</style>
