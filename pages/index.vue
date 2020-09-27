<template>
<section>
  <Divider />
  <ServicesList />
</section>
</template>

<script>
import Divider from "@/components/Divider";
import ServicesList from "@/components/ServicesList";
export default {
  props:{
  },
  components: {
    Divider,
    ServicesList,
  }
};
</script>

<style lang="scss" scoped>

</style>