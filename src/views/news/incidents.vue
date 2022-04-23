<template>
<newsmenu />
<div v-for="item in getArt" :key="item.heading" class="card">
  <h5 class="card-header">{{item.heading}}</h5>
  <div class="card-body">
    <p class="card-text">{{item.description}}</p>
   <router-link class="btn btn-primary"   :to="{name: 'article', params:{id: item.id }}">Подробнее...</router-link> 
  </div>
  </div>


</template>
<script>
import newsmenu from '@/components/newsmenu.vue'
export default{
    name: 'incidents',
    components:{
        newsmenu
    },
    computed:{
        getArt(){
            return this.$store.getters.getArticle
        }
    }
}
</script>