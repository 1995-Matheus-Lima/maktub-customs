
<template >
  <div class="item">
    <v-icon class="icon">{{item.img}}</v-icon>
    <NuxtLink :to="`/${item.route}`">
      <h3 class="item-link">{{item.title}}</h3>
    </NuxtLink>
    <p class="description">{{item.description}}</p>
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
  .v-application a {
    text-decoration: none;
    color: black;
  }

  .description {
    text-align: justify;
    margin-top: 1vmin;
  }
    
  .multi-item{
    border: 1px solid ;
    border-radius: 20%;
    padding:5px 10px;
    color:#252525;
    margin-top:20px;
    
  }
  .multi-item:hover,
  .item-link:hover
  {
     color:#E49061;
   }
  
</style>