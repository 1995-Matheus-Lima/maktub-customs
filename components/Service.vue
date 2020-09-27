
<template >
  <div class="item">
    <img :src="`service/${item.img}`" />
    <h3>{{item.title}}</h3>
    <h4></h4>
    <NuxtLink :to="`/${item.route}`">
      <button class="multi-item">  View Item </button>
    </NuxtLink>
  </div>
</template>

<script>
    export default {
        props:{
            item:{
                default: () =>({
                  img: 'calendar',
                  route: 'agenda',
                  title: 'Agende seu horario'
                })
            }
        }
    }
</script>

<style lang="scss" scoped>
  .item{
    box-sizing:border-box;
    width:300px;
    height:250px;
    margin:40px 20px 40px 0;
    text-align:center;
    padding:20px;
    border: 1px solid rgba(000,000,000,.3);
    box-shadow: 1px 1px 1px #252525;
  }
  img{
    width:100px;
    height:100px;
  }
  template::before,template::after{
    contain:"";
    display:table;
    clear:both
  }
  .multi-item{
    border: 1px solid ;
    border-radius: 20%;
    padding:5px 10px;
    color:#252525;
    margin-top:20px;
    
  }
  .multi-item:hover{
     color:#E49061;
   }
  
</style>