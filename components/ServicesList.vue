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
            img: 'calentar',
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