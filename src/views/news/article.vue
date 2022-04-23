<template>
<div class="container">
<div class="row">
    {{Art}}

  <p> autor </p>

</div>
</div>
</template>
<script>
export default {
    name: 'article',
    Data(){
      return{
            article:''
      }
    },
    props:['id'],
    computed:{
       Art(){
            return   this.$store.getters.getItemArt(this.id)
       }
    }
}
</script>