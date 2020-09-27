<template>
  <section >
    <div class="container-item">
      <div  v-for="serv in services" :key=serv.id>
        <Service  :item="serv" />  
      </div>
    </div>
  </section>
</template>

<script>
  import Service from "@/components/Service";
  export default {
    props: {
      services: {
        default: () => [
          {
            id: 'agenda',
            img: 'mdi-calendar',
            route: 'agenda',
            title: 'Agende seu horario'
          },
          {
            id: 'consulta',
            img: 'mdi-book-search-outline',
            route: 'consulta',
            title: 'Consulte o status'
          },
          {
            id: 'catalogo',
            img: 'mdi-newspaper-variant-multiple',
            route: 'catalogo',
            title: 'Veja o catalogo'
          }, 
      ]
    },
  },
  components: {
    Service
  }
}
</script>
  
<style lang="scss" scoped>
 .container-item{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin: 0 auto;
  }

</style>