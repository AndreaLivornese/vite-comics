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


</style>
