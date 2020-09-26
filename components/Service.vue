<template>
   <div class="item">
        <img :src="`/services/${item.img}`" />
        <h3>{{item.title}}</h3>
        <h4></h4>
        <NuxtLink :to="`/${item.route}`">
          <button class="multi-item">View Item ></button>
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

</style>