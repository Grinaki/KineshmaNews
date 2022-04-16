<template>
<div class="container">
<div class="row">
<h1> Заголовк </h1>
       {{id}}
<p>{
    path: '/histori/:id',
    components: HistoryId,
    name: 'historyId',
    props: true   
}</p>

  <p> autor </p>

</div>
</div>
</template>
<script>
export default {
    name: 'article',
    props:['id']
}
</script>