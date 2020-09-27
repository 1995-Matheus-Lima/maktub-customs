<template>
  <section >
    <div class="container-item">
      <div  v-for="serv in services" :key=serv.id>
        <Service  :item="serv" />  
      </div>
      <WhatsappContact />
    </div>
  </section>
</template>

<script>
  import Service from "@/components/Service";
  import Whats from "@/components/Whats";
  export default {
    props: {
      services: {
        default: () => [
          {
            id: 'agenda',
            img: 'mdi-calendar',
            route: 'agenda',
            title: 'Agende seu horario',
            description: 'Agende seu horario online! The landscape dump braked the mechanical upfitted the work-ready'
          },
          {
            id: 'consulta',
            img: 'mdi-book-search-outline',
            route: 'consulta',
            title: 'Consulte o status',
            description: 'Seu carro está em nossos cuidados ou pediu um orçamento? Consulte o status do serviço aqui!'
          },
          {
            id: 'catalogo',
            img: 'mdi-newspaper-variant-multiple',
            route: 'catalogo',
            title: 'Veja o catalogo',
            description: 'Procurando inspiração? Dá uma olhadinha no nosso catálogo com essas ideias boooooas'
          }, 
      ]
    },
  },
  components: {
    Service, 
    Whats
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