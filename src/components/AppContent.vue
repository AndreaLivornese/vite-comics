<script>

export default{
  name:"AppContent",

  data(){
    return{
       
        content: "--> Content goes here <--",

    }
  },
}
</script>

<template>
 
<section class="sec-content">

    <div class="container">
    
    <div class="content">
     {{ content }}
    </div>

    </div>

</section>

</template>

<style lang="scss">
@use '../style/mixins' as *;


.content{
    font-size: 20px;
    color:white;
    font-weight: bold;
}

.sec-content{
    padding: 56px 0;
    background-color: black;
}


</style>
