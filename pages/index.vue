<template>
<section>
  <Divider />
  <div class="item" v-for="serv in services" :key=serv.id>
    <img :src="`/services/${serv.img}`" />
    <h3>{{serv.title}}</h3>
    <h4></h4>
    <NuxtLink :to="`/${serv.route}`">
      <button class="multi-item">View Item ></button>
    </NuxtLink>
  </div>
</section>
</template>

<script>
import Divider from "@/components/Divider";
export default {
  props: {
    services: {
      default: () => [
        {
          id: 'agenda',
          img: 'calendar',
          route: 'agenda',
          title: 'Agende seu horario'
        },
        {
          id: 'consulta',
          img: 'consulta',
          route: 'consulta',
          title: 'Consulte o status'
        },
        {
          id: 'catalogo',
          img: 'catalogo',
          route: 'catalogo',
          title: 'Veja o catalogo'
        },
        
      ]
    },
  },
  components: {
    Divider
  }
};
</script>

<style lang="scss" scoped>

</style>