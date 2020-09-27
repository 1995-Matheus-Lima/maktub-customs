<template>
<section>
  <Divider />
  <ServicesList />
</section>
</template>

<script>
import Divider from "@/components/Divider";
import ServicesList from "@/components/ServicesList";
import WhatsappContact from "@/components/WhatsappContact";
export default {
  props:{
  },
  components: {
    Divider,
    ServicesList,
    WhatsappContact
  }
};
</script>

<style lang="scss" scoped>

</style>