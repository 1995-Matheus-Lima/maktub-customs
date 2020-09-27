
<template >
  <div class="item">
    <v-icon class="icon">{{item.img}}</v-icon>
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
    border-top: 1px solid #bdbdbd57;
    border-left: 1px solid #bdbdbd57;
    box-shadow: 2px 2px 3px 0px #25252570;
  }
  .icon {
    font-size: 56px;
    color: #E49061
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